# Billit: Get Party

Retrieves a Billit party by ID.

```
GET https://connect.mindcloud.co/v1/universal/billit/latest/actions/get-party
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Billit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/billit/latest/actions/get-party?connectionId=$CONNECTION_ID&partyID=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "partyID": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/billit/latest/actions/get-party?${params}`, {
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
| `partyID` | number | yes | Billit PartyID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Addresses": [
        {}
      ],
      "DisplayName": "Ava Chen",
      "Name": "Ava Chen",
      "PartyID": 1,
      "PartyType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Addresses` | array<object> | Addresses linked to the party. |
| `DisplayName` | string | Billit display name. |
| `Name` | string | Billit party display name. |
| `PartyID` | number | Billit party identifier. |
| `PartyType` | string | Billit party type. |

## Native endpoint

Through the native Billit API, this operation is `GET /v1/parties/:partyID` (base URL `https://api.sandbox.billit.be`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-party.md) for the provider-specific parameters and requirements.

