# TouchBasePro: Import Subscribers

Imports subscribers into your TouchBasePro account.

```
POST https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/import-subscribers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TouchBasePro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/import-subscribers" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/import-subscribers', {
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
      "duplicateEmailsInSubmission": [
        [
          "ava@example.com"
        ]
      ],
      "failureDetails": [
        [
          "string"
        ]
      ],
      "totalExistingSubscribers": 1,
      "totalNewSubscribers": 1,
      "totalUniqueEmailsSubmitted": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `duplicateEmailsInSubmission[]` | array<string> |  |
| `failureDetails[]` | array<string> |  |
| `totalExistingSubscribers` | number |  |
| `totalNewSubscribers` | number |  |
| `totalUniqueEmailsSubmitted` | number |  |

## Native endpoint

Through the native TouchBasePro API, this operation is `POST /email/subscribers/{listId}/import` (base URL `https://api.touchbasepro.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/import-subscribers.md) for the provider-specific parameters and requirements.

