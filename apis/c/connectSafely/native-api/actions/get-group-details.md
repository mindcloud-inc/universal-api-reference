# Get group details with ConnectSafely

Retrieve detailed information about a specific LinkedIn group including full description, rules, member count, activity level, and admin information.

## Endpoint

- **Method:** `POST`
- **Path:** `/search/groups/details`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Get group details](https://connectsafely.ai/docs/api/linkedin-search/post-search-groups-details-get-group-details)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | body | `string` | no | LinkedIn account ID to use. If not provided, uses the default account. |
| `groupId` | body | `string` | yes | LinkedIn group ID from search results or group page URL |

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | `boolean` |  |
| `group` | `object` | Group details with member insights |
| `group.memberInsights` | `array` | Insights about group members (education, location, industry) |
| `group.memberInsights[].insight` | `string` | Description of the insight (e.g., "Are located in India") |
| `group.memberInsights[].count` | `number` | Number of members matching this insight |
| `group.totalInsights` | `number` | Total number of insights returned |

### Example response

```json
{
  "success": true,
  "group": {
    "memberInsights": [
      {
        "insight": "Attended Pune University",
        "count": 55
      },
      {
        "insight": "Are located in India",
        "count": 30295
      },
      {
        "insight": "Are in the Computer Software industry",
        "count": 14488
      }
    ],
    "totalInsights": 3
  }
}
```

## Error status codes

`400`, `401`, `500`. Bodies follow the shared `{ success, code, message }` error shape.
