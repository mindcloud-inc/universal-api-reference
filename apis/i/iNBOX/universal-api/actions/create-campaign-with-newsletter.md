# INBOX: Create Campaign With Newsletter

Creates a new INBOX campaign from a newsletter.

```
POST https://connect.mindcloud.co/v1/universal/iNBOX/latest/actions/create-campaign-with-newsletter
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a INBOX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/iNBOX/latest/actions/create-campaign-with-newsletter" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/iNBOX/latest/actions/create-campaign-with-newsletter', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "resultCode": 1,
      "resultMessage": "string",
      "resultObject": "string",
      "resultStatus": true,
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `resultCode` | number |  |
| `resultMessage` | string |  |
| `resultObject` | string |  |
| `resultStatus` | boolean |  |
| `version` | string |  |

## Native endpoint

Through the native INBOX API, this operation is `POST /inbox/v1/campaigns` (base URL `https://useapi.useinbox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-campaign-with-newsletter.md) for the provider-specific parameters and requirements.

