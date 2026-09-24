# ADP: List Worker Time Off Balances



```
GET https://connect.mindcloud.co/v1/universal/adp/latest/actions/list-worker-time-off-balances
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ADP `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/adp/latest/actions/list-worker-time-off-balances?connectionId=$CONNECTION_ID&aoid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "aoid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/adp/latest/actions/list-worker-time-off-balances?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `aoid` | string | yes | The ADP associate object identifier for the worker whose time-off balances should be returned. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "asOfDate": "string",
      "paidTimeOffPolicyBalances": [
        {
          "paidTimeOffPolicy": {
            "code": "string",
            "labelName": "Ava Chen"
          },
          "policyBalances": [
            {
              "balanceType": {
                "code": "string",
                "labelName": "Ava Chen"
              },
              "totalQuantity": {
                "labelName": "Ava Chen",
                "unitTimeCode": "string",
                "valueNumber": 1
              }
            }
          ]
        }
      ],
      "positionRef": {
        "positionID": {
          "id": "string",
          "schemeAgencyName": "Ava Chen",
          "schemeName": "Ava Chen"
        },
        "title": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `asOfDate` | string |  |
| `paidTimeOffPolicyBalances[].paidTimeOffPolicy.code` | string |  |
| `paidTimeOffPolicyBalances[].paidTimeOffPolicy.labelName` | string |  |
| `paidTimeOffPolicyBalances[].policyBalances[].balanceType.code` | string |  |
| `paidTimeOffPolicyBalances[].policyBalances[].balanceType.labelName` | string |  |
| `paidTimeOffPolicyBalances[].policyBalances[].totalQuantity.labelName` | string |  |
| `paidTimeOffPolicyBalances[].policyBalances[].totalQuantity.unitTimeCode` | string |  |
| `paidTimeOffPolicyBalances[].policyBalances[].totalQuantity.valueNumber` | number |  |
| `positionRef.positionID.id` | string |  |
| `positionRef.positionID.schemeAgencyName` | string |  |
| `positionRef.positionID.schemeName` | string |  |
| `positionRef.title` | string |  |

## Native endpoint

Through the native ADP API, this operation is `GET time/v2/workers/:aoid/time-off-details/time-off-balances` (base URL `https://api.adp.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-worker-time-off-balances.md) for the provider-specific parameters and requirements.

