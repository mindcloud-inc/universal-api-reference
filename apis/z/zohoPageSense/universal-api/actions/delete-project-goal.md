# Zoho PageSense: Delete Project Goal

Deletes a project goal from Zoho PageSense.

```
DELETE https://connect.mindcloud.co/v1/universal/zohoPageSense/latest/actions/delete-project-goal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho PageSense `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/zohoPageSense/latest/actions/delete-project-goal?connectionId=$CONNECTION_ID&portalName=Ava%20Chen&projectLinkname=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "portalName": "Ava Chen",
  "projectLinkname": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoPageSense/latest/actions/delete-project-goal?${params}`, {
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
          "goalId": 1,
          "goalStatus": 1,
          "linkname": "https://example.com",
          "projectLinkname": "https://example.com",
          "success": true
        }
      ],
      "statusCode": "string",
      "statusString": "string",
      "timeTakenToProcessTheRequest": "string"
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
| `projectgoals[].goalId` | number |  |
| `projectgoals[].goalStatus` | number |  |
| `projectgoals[].linkname` | string |  |
| `projectgoals[].projectLinkname` | string |  |
| `projectgoals[].success` | boolean |  |
| `statusCode` | string |  |
| `statusString` | string |  |
| `timeTakenToProcessTheRequest` | string |  |

## Native endpoint

Through the native Zoho PageSense API, this operation is `DELETE /portal/:portalName/projectgoals/:projectLinkname` (base URL `https://pagesense.zoho.com/pagesense/rest/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-project-goal.md) for the provider-specific parameters and requirements.

