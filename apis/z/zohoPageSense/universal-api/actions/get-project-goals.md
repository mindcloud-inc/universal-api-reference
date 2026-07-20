# Zoho PageSense: Get Project Goals

Retrieves project goals from Zoho PageSense.

```
GET https://connect.mindcloud.co/v1/universal/zohoPageSense/latest/actions/get-project-goals
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho PageSense `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoPageSense/latest/actions/get-project-goals?connectionId=$CONNECTION_ID&portalName=Ava%20Chen&projectLinkname=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "portalName": "Ava Chen",
  "projectLinkname": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoPageSense/latest/actions/get-project-goals?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `portalName` | string | yes | Portal identifier in the path. |
| `projectLinkname` | string | yes | Project linkname in the path. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "projectgoals": [
        {
          "displayName": "Ava Chen",
          "elementCssSelector": "string",
          "goalStatus": 1,
          "goalType": 1,
          "goalUrl": "https://example.com",
          "linkname": "https://example.com"
        }
      ],
      "statusCode": "string",
      "statusString": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `projectgoals[].displayName` | string |  |
| `projectgoals[].elementCssSelector` | string |  |
| `projectgoals[].goalStatus` | number |  |
| `projectgoals[].goalType` | number |  |
| `projectgoals[].goalUrl` | string |  |
| `projectgoals[].linkname` | string |  |
| `statusCode` | string |  |
| `statusString` | string |  |

## Native endpoint

Through the native Zoho PageSense API, this operation is `GET /portal/:portalName/projectgoals/:projectLinkname` (base URL `https://pagesense.zoho.com/pagesense/rest/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-goals.md) for the provider-specific parameters and requirements.

