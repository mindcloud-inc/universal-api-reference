# Get connections list with ConnectSafely

Retrieves the list of LinkedIn connections for the authenticated user. Returns connection details including name, headline, vanity name, and connected date. Supports pagination via startIndex and limit parameters. **Paginating clients must stop on `endOfList: true`, not on an empty array** — an empty page with HTTP 502 / `code: CONNECTIONS_UNAVAILABLE` means LinkedIn temporarily returned nothing and the request should be retried.

## Endpoint

- **Method:** `GET`
- **Path:** `/connections`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Get connections list](https://connectsafely.ai/docs/api/linkedin-user/get-connections-get-connections)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | query | `string` | no | LinkedIn account ID to use. If not provided, uses the default account. |
| `startIndex` | query | `number` | no | Starting index for pagination (0-indexed). Use to fetch additional connections. Default: `0`. |
| `limit` | query | `number` | no | Number of connections to return (max 12). Default: `10`. |
| `sortBy` | query | `list` | no | Sort order for connections. Options: recentlyAdded (default), firstName, lastName. Accepted values: `recentlyAdded`, `firstName`, `lastName`. Default: `recentlyAdded`. |

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | `boolean` |  |
| `connections` | `array` |  |
| `connections[].firstName` | `string` | First name of the connection |
| `connections[].lastName` | `string` | Last name of the connection |
| `connections[].vanityName` | `string` | LinkedIn vanity name (profile slug) |
| `connections[].headline` | `string` | Professional headline |
| `connections[].connectedDate` | `string` | Date when the connection was made |
| `connections[].profileUrl` | `string` | Full LinkedIn profile URL |
| `endOfList` | `boolean` | true only when this page is empty AND the account has no connections beyond startIndex (verified against the exact connection count). Paginate until this is true — never stop on an empty array alone. |
| `startIndex` | `number` | Starting index used for this request |
| `limit` | `number` | Number of items requested |
| `sortBy` | `list` | Sort order applied to connections |
| `accountId` | `string` | LinkedIn account ID used for the request |

### Example response

```json
{
  "success": true,
  "endOfList": false,
  "connections": [
    {
      "firstName": "John",
      "lastName": "Doe",
      "vanityName": "johndoe",
      "headline": "CEO | Entrepreneur | Tech Founder",
      "connectedDate": "Connected on Feb 15, 2024",
      "profileUrl": "https://www.linkedin.com/in/johndoe/"
    },
    {
      "firstName": "Jane",
      "lastName": "Smith",
      "vanityName": "janesmith",
      "headline": "VP of Engineering at TechCorp",
      "connectedDate": "Connected on Jan 10, 2024",
      "profileUrl": "https://www.linkedin.com/in/janesmith/"
    }
  ],
  "startIndex": 0,
  "limit": 10,
  "sortBy": "recentlyAdded",
  "accountId": "696ce9e780e0483585e4e553"
}
```

## Error status codes

`401`, `500`, `502`. Bodies follow the shared `{ success, code, message }` error shape.
