# jo4.io: Record Conversion



```
POST https://connect.mindcloud.co/v1/universal/jo4io/latest/actions/record-conversion-1
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a jo4.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/jo4io/latest/actions/record-conversion-1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "slug": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/jo4io/latest/actions/record-conversion-1', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "slug": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `currency` | string | no |  |
| `eventType` | string | no |  |
| `externalId` | string | no |  |
| `metadata` | string | no |  |
| `quantity` | number | no |  |
| `slug` | string | yes |  |
| `value` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributionModel": "string",
      "attributionWindowDays": 1,
      "bioId": 1,
      "city": "string",
      "clickId": 1,
      "clickTime": 1,
      "conversionTime": 1,
      "country": "string",
      "createdTime": 1,
      "currency": "string",
      "deviceType": "string",
      "eventType": "string",
      "externalId": "string",
      "id": 1,
      "metadata": "string",
      "modifiedTime": 1,
      "quantity": 1,
      "slug": "string",
      "source": "string",
      "teamId": 1,
      "timeToConvert": 1,
      "urlId": 1,
      "userId": 1,
      "value": 1,
      "verificationStatus": "string",
      "verified": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributionModel` | string |  |
| `attributionWindowDays` | number |  |
| `bioId` | number |  |
| `city` | string |  |
| `clickId` | number |  |
| `clickTime` | number |  |
| `conversionTime` | number |  |
| `country` | string |  |
| `createdTime` | number |  |
| `currency` | string |  |
| `deviceType` | string |  |
| `eventType` | string |  |
| `externalId` | string |  |
| `id` | number |  |
| `metadata` | string |  |
| `modifiedTime` | number |  |
| `quantity` | number |  |
| `slug` | string |  |
| `source` | string |  |
| `teamId` | number |  |
| `timeToConvert` | number |  |
| `urlId` | number |  |
| `userId` | number |  |
| `value` | number |  |
| `verificationStatus` | string |  |
| `verified` | boolean |  |

## Native endpoint

Through the native jo4.io API, this operation is `POST /protected/url/:slug/conversions` (base URL `https://jo4-api.jo4.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/record-conversion-1.md) for the provider-specific parameters and requirements.

