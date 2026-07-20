# Bridge Interactive Platform: Get member (OData)

Retrieves a member from Bridge Interactive Platform.

```
GET https://connect.mindcloud.co/v1/universal/bridgeInteractivePlatform/latest/actions/get-member-o-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bridge Interactive Platform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bridgeInteractivePlatform/latest/actions/get-member-o-data?connectionId=$CONNECTION_ID&dataset=test&MemberKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dataset": "test",
  "MemberKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bridgeInteractivePlatform/latest/actions/get-member-o-data?${params}`, {
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
| `dataset` | string | yes | Bridge dataset code. This tenant was validated against dataset test. Default: `test`. |
| `MemberKey` | string | yes | OData member identifier from Bridge. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "MemberEmail": "ava@example.com",
      "MemberFullName": "Ava Chen",
      "MemberKey": "string",
      "MemberMlsId": "string",
      "MemberStatus": "string",
      "OfficeKey": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `MemberEmail` | string |  |
| `MemberFullName` | string |  |
| `MemberKey` | string |  |
| `MemberMlsId` | string |  |
| `MemberStatus` | string |  |
| `OfficeKey` | string |  |

## Native endpoint

Through the native Bridge Interactive Platform API, this operation is `GET /OData/:dataset/Member(':MemberKey')` (base URL `https://api.bridgedataoutput.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-member-o-data.md) for the provider-specific parameters and requirements.

