# PostcardMania: Get Design

Retrieves a design from PostcardMania.

```
GET https://connect.mindcloud.co/v1/universal/postcardMania/latest/actions/get-design
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PostcardMania `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/postcardMania/latest/actions/get-design?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/postcardMania/latest/actions/get-design?${params}`, {
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
| `designID` | string | no | Numeric PostcardMania design identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "approvalDateTime": "2026-05-07T12:00:00.000Z",
      "designFields": [
        {}
      ],
      "designID": 1,
      "friendlyName": "Ava Chen",
      "mailClasses": [
        "string"
      ],
      "productType": "string",
      "proofBack": "string",
      "proofFront": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `approvalDateTime` | date | Approval timestamp. |
| `designFields` | array<object> | Design merge fields. |
| `designID` | number | Design identifier. |
| `friendlyName` | string | Design display name. |
| `mailClasses` | array<string> | Available mail classes. |
| `productType` | string | Design product type. |
| `proofBack` | string | Back proof image URL. |
| `proofFront` | string | Front proof image URL. |

## Native endpoint

Through the native PostcardMania API, this operation is `GET /design/{{designID}}` (base URL `https://v3.pcmintegrations.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-design.md) for the provider-specific parameters and requirements.

