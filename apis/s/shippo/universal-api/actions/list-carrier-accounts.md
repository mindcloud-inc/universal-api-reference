# Shippo - Legacy: List Carrier Accounts

Retrieves carrier accounts connected to your Shippo account.

```
GET https://connect.mindcloud.co/v1/universal/shippo/latest/actions/list-carrier-accounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shippo - Legacy `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shippo/latest/actions/list-carrier-accounts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shippo/latest/actions/list-carrier-accounts?${params}`, {
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
| `results` | number | no | Set how many carrier accounts to return per page. |
| `serviceLevels` | boolean | no | Include service levels for each returned carrier account. |
| `carrier` | string | no | Filter carrier accounts by carrier token. |
| `accountId` | string | no | Filter the response by carrier account ID. |
| `page` | number | no | Select which page of carrier accounts to return. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `apiKey` | string | no | Override the authentication API key here |

## Response

```json
{
  "success": true,
  "data": [
    {
      "next": "string",
      "previous": {},
      "results": [
        {
          "accountId": "string",
          "active": true,
          "carrier": "string",
          "carrierImages": {
            "75": "string",
            "200": "string"
          },
          "carrierName": "Ava Chen",
          "isShippoAccount": true,
          "metadata": "string",
          "objectId": "string",
          "objectInfo": {
            "authentication": {
              "type": "string"
            }
          },
          "objectOwner": "string",
          "test": true
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `next` | string |  |
| `previous` | object |  |
| `results[].accountId` | string |  |
| `results[].active` | boolean |  |
| `results[].carrier` | string |  |
| `results[].carrierImages.200` | string |  |
| `results[].carrierImages.75` | string |  |
| `results[].carrierName` | string |  |
| `results[].isShippoAccount` | boolean |  |
| `results[].metadata` | string |  |
| `results[].objectId` | string |  |
| `results[].objectInfo.authentication.type` | string |  |
| `results[].objectOwner` | string |  |
| `results[].test` | boolean |  |

## Native endpoint

Through the native Shippo - Legacy API, this operation is `GET /carrier_accounts` (base URL `https://api.goshippo.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-carrier-accounts.md) for the provider-specific parameters and requirements.

