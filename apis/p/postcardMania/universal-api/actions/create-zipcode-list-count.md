# PostcardMania: Create Zipcode List Count

Creates a ZIP code list count in PostcardMania.

```
POST https://connect.mindcloud.co/v1/universal/postcardMania/latest/actions/create-zipcode-list-count
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PostcardMania `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/postcardMania/latest/actions/create-zipcode-list-count" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/postcardMania/latest/actions/create-zipcode-list-count', {
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `breakdownType` | string | no | One of ZipCode, ZipCrrt, or Gender. |
| `demographics[]` | array<object> | no | Array of demographic filter objects. Use an empty array for no filters. |
| `listType` | string | no | PostcardMania list type key such as IRL. |
| `zipCodes[]` | array<string> | no | Array of ZIP code strings. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "breakdown": [
        {}
      ],
      "listCountID": 1,
      "recordCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `breakdown` | array<object> | Breakdown buckets returned by PCM. |
| `listCountID` | number | PostcardMania list count identifier. |
| `recordCount` | number | Total matching records. |

## Native endpoint

Through the native PostcardMania API, this operation is `POST /list/count/zipcode` (base URL `https://v3.pcmintegrations.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-zipcode-list-count.md) for the provider-specific parameters and requirements.

