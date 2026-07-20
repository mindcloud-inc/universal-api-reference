# Zoho PageSense: Update Experiment Audience

Updates experiment audience settings in Zoho PageSense.

```
PUT https://connect.mindcloud.co/v1/universal/zohoPageSense/latest/actions/update-experiment-audience
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho PageSense `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zohoPageSense/latest/actions/update-experiment-audience" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "portalName": "Ava Chen",
  "experimentLinkname": "https://example.com",
  "experimentaudience": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoPageSense/latest/actions/update-experiment-audience', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "portalName": "Ava Chen",
    "experimentLinkname": "https://example.com",
    "experimentaudience": "string"
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
| `experimentaudience` | string | yes | Audience assignment payload for the experiment. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "experimentaudience": [
        {
          "experimentId": 1,
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
| `experimentaudience[].experimentId` | number |  |
| `experimentaudience[].success` | boolean |  |
| `statusCode` | string |  |
| `statusString` | string |  |
| `timeTakenToProcessTheRequest` | string |  |

## Native endpoint

Through the native Zoho PageSense API, this operation is `PUT https://pagesense.zoho.com/pagesense/api/v1/portal/:portalName/experimentaudience/:experimentLinkname` (base URL `https://pagesense.zoho.com/pagesense/rest/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-experiment-audience.md) for the provider-specific parameters and requirements.

