# RollWorks: List Target Accounts List Names and EIDs

Retrieves target account list names and EIDs from RollWorks.

```
GET https://connect.mindcloud.co/v1/universal/rollWorks/latest/actions/list-target-accounts-list-names-and-eids
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RollWorks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rollWorks/latest/actions/list-target-accounts-list-names-and-eids?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rollWorks/latest/actions/list-target-accounts-list-names-and-eids?${params}`, {
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
      "data": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |

## Native endpoint

Through the native RollWorks API, this operation is `GET /audience/v1/target_accounts/names` (base URL `https://services.adroll.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-target-accounts-list-names-and-eids.md) for the provider-specific parameters and requirements.

