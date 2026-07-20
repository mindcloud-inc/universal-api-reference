# IdentityCheck: Get Verification Chart



```
GET https://connect.mindcloud.co/v1/universal/identityCheck/latest/actions/get-verification-chart
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IdentityCheck `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/identityCheck/latest/actions/get-verification-chart?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/identityCheck/latest/actions/get-verification-chart?${params}`, {
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
      "datasets": [
        {
          "data": [
            1
          ],
          "label": "string"
        }
      ],
      "labels": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `datasets[].data[]` | number |  |
| `datasets[].label` | string |  |
| `labels[]` | string |  |

## Native endpoint

Through the native IdentityCheck API, this operation is `GET /verification/chart` (base URL `https://identity.stackgo.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-verification-chart.md) for the provider-specific parameters and requirements.

