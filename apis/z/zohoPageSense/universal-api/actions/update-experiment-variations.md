# Zoho PageSense: Update Experiment Variations

Updates experiment variations in Zoho PageSense.

```
PUT https://connect.mindcloud.co/v1/universal/zohoPageSense/latest/actions/update-experiment-variations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho PageSense `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zohoPageSense/latest/actions/update-experiment-variations" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "portalName": "Ava Chen",
  "experimentLinkname": "https://example.com",
  "experiment": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoPageSense/latest/actions/update-experiment-variations', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "portalName": "Ava Chen",
    "experimentLinkname": "https://example.com",
    "experiment": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `portalName` | string | yes | Portal identifier in the path. |
| `experimentLinkname` | string | yes | Experiment linkname in the path. |
| `experiment` | string | yes | Experiment object containing variation updates. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "experiments": [
        {
          "displayName": "Ava Chen",
          "experimentId": "string",
          "experimentKey": "string",
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
| `experiments[].displayName` | string |  |
| `experiments[].experimentId` | string |  |
| `experiments[].experimentKey` | string |  |
| `experiments[].linkname` | string |  |
| `experiments[].projectLinkname` | string |  |
| `experiments[].success` | boolean |  |
| `statusCode` | string |  |
| `statusString` | string |  |
| `timeTakenToProcessTheRequest` | string |  |

## Native endpoint

Through the native Zoho PageSense API, this operation is `PUT /portal/:portalName/experiments/:experimentLinkname` (base URL `https://pagesense.zoho.com/pagesense/rest/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-experiment-variations.md) for the provider-specific parameters and requirements.

