# AbcSubmit: Get My Stats

Retrieves your current AbcSubmit plan usage.

```
GET https://connect.mindcloud.co/v1/universal/abcSubmit/latest/actions/get-my-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AbcSubmit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/abcSubmit/latest/actions/get-my-stats?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/abcSubmit/latest/actions/get-my-stats?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "formsCount": 1,
      "mailsSentDaily": 1,
      "storageNumFiles": 1,
      "storageQuota": 1,
      "submissionsCount": 1,
      "subuserAccounts": 1,
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `formsCount` | number |  |
| `mailsSentDaily` | number |  |
| `storageNumFiles` | number |  |
| `storageQuota` | number |  |
| `submissionsCount` | number |  |
| `subuserAccounts` | number |  |
| `userId` | number |  |

## Native endpoint

Through the native AbcSubmit API, this operation is `GET /api/v1/users/my-stats` (base URL `https://www.abcsubmit.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-my-stats.md) for the provider-specific parameters and requirements.

