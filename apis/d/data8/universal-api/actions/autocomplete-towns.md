# Data8: Autocomplete Towns

Finds town name suggestions in Data8.

```
GET https://connect.mindcloud.co/v1/universal/data8/latest/actions/autocomplete-towns
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Data8 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/data8/latest/actions/autocomplete-towns?connectionId=$CONNECTION_ID&licence=string&townName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "licence": "string",
  "townName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/data8/latest/actions/autocomplete-towns?${params}`, {
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
| `licence` | string | yes | The licence type under which you are accessing the service. |
| `townName` | string | yes | The town name to autocomplete. |
| `options` | object | no | Optional settings that control location lookup behavior. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Status": {
        "CreditsRemaining": 1,
        "ErrorMessage": "string",
        "Success": true
      },
      "Towns": [
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
| `Status.CreditsRemaining` | number |  |
| `Status.ErrorMessage` | string |  |
| `Status.Success` | boolean |  |
| `Towns[]` | string |  |

## Native endpoint

Through the native Data8 API, this operation is `POST /Location/AutoCompleteTowns.json` (base URL `https://webservices.data-8.co.uk`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/autocomplete-towns.md) for the provider-specific parameters and requirements.

