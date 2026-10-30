# ServiceTitan: Mark AP Credits as Exported

Marks the specified AP credits as exported in ServiceTitan.

```
PUT https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/mark-ap-credits-as-exported
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServiceTitan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/mark-ap-credits-as-exported" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "apCredits[].apCreditId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/mark-ap-credits-as-exported', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "apCredits[].apCreditId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `apCredits[]` | array<object> | no |  |
| `apCredits[].apCreditId` | list<number> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apCreditId": 1,
      "errorMessage": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apCreditId` | number |  |
| `errorMessage` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native ServiceTitan API, this operation is `POST accounting/v2/tenant/{{credentials.tenant}}/ap-credits/markasexported` (base URL `https://{{credentials.baseUrl}}/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/mark-ap-credits-as-exported.md) for the provider-specific parameters and requirements.

