# API Documentation: GET /lead/

## Description
The `GET /lead/` endpoint retrieves lead data based on various filtering and sorting criteria.

## Request

### Headers
- **Content-Type**: `application/json`
- **x-api-key**: `your API key`

### Query Parameters
| Parameter        | Type       | Default Value | Allowed Values / Format                                      | Description |
|-----------------|-----------|--------------|-------------------------------------------------------------|-------------|
| `page`         | `integer`  | `0`          | Any non-negative integer                                    | Page number starting from 0. |
| `size`         | `integer`  | `100`        | Maximum: `1000`                                            | Number of records per page. |
| `sort`         | `string`   | `createdAt,desc` | `createdAt` or `lastExternalStatusAt`, direction: `asc` or `desc` | Sorting field and direction, separated by a comma. Examples: `createdAt,asc`, `lastExternalStatusAt,desc`. |
| `createdFrom`   | `dateTime` | None         | `yyyy-MM-dd'T'HH:mm:ss` Example: `2024-02-13T19:49:54`     | Filter results by creation date (starting from). If not provided, data will not be filtered. |
| `createdTo`     | `dateTime` | None         | `yyyy-MM-dd'T'HH:mm:ss` Example: `2025-11-02T02:02:20`     | Filter results by creation date (up to). If not provided, data will not be filtered. |

## Response
The response will return a JSON object containing the lead data that matches the given filtering and sorting criteria.

