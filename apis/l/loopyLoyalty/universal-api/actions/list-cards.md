# Loopy Loyalty: List Cards



```
GET https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/list-cards
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loopy Loyalty `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/list-cards?connectionId=$CONNECTION_ID&cid=5fcDywPejwj9QszwngBTKg" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "cid": "5fcDywPejwj9QszwngBTKg"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/list-cards?${params}`, {
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
| `cid` | string | yes | Campaign ID to list cards for. Example: `5fcDywPejwj9QszwngBTKg`. |
| `start` | number | no | Zero-based row offset for pagination. Example: `0`. |
| `length` | number | no | Number of cards to return. Example: `10`. |
| `search` | string | no | Optional search term applied across customer details. Example: `Taylor`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data[0]": {
        "campaignId": "string",
        "created": "string",
        "currentStamps": 1,
        "customerDetails": {
          "Email Address": "ava@example.com",
          "First Name": "Ava Chen",
          "Mobile Number": "string"
        },
        "id": "string",
        "status": "string",
        "updated": "string"
      },
      "recordsFiltered": 1,
      "recordsTotal": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[0].campaignId` | string | Campaign ID the card belongs to. |
| `data[0].created` | string | Card created timestamp. |
| `data[0].currentStamps` | number | Current stamp count. |
| `data[0].customerDetails.Email Address` | string | Customer email address. |
| `data[0].customerDetails.First Name` | string | Customer first name. |
| `data[0].customerDetails.Mobile Number` | string | Customer mobile number. |
| `data[0].id` | string | Card ID. |
| `data[0].status` | string | Card pass status. |
| `data[0].updated` | string | Card updated timestamp. |
| `recordsFiltered` | number | Total cards after applying search. |
| `recordsTotal` | number | Total cards returned for the query. |

## Native endpoint

Through the native Loopy Loyalty API, this operation is `POST /card/cid/:cid` (base URL `https://api.loopyloyalty.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-cards.md) for the provider-specific parameters and requirements.

