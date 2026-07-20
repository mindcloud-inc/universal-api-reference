# Data8: Parse Name

Parses a submitted name with Data8.

```
GET https://connect.mindcloud.co/v1/universal/data8/latest/actions/parse-name
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Data8 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/data8/latest/actions/parse-name?connectionId=$CONNECTION_ID&name=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "name": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/data8/latest/actions/parse-name?${params}`, {
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
| `name` | string | yes | The name string to parse. |
| `options` | object | no | Optional settings that control name parsing behavior. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "FormalSalutation": "string",
      "Gender": "string",
      "InformalSalutation": "string",
      "Name": {
        "Forename": "Ava Chen",
        "Surname": "Ava Chen",
        "Title": "Ava Chen"
      },
      "Status": {
        "CreditsRemaining": 1,
        "ErrorMessage": "string",
        "Success": true
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `FormalSalutation` | string |  |
| `Gender` | string |  |
| `InformalSalutation` | string |  |
| `Name.Forename` | string |  |
| `Name.Surname` | string |  |
| `Name.Title` | string |  |
| `Status.CreditsRemaining` | number |  |
| `Status.ErrorMessage` | string |  |
| `Status.Success` | boolean |  |

## Native endpoint

Through the native Data8 API, this operation is `POST /NameCleansing/ParseName.json` (base URL `https://webservices.data-8.co.uk`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/parse-name.md) for the provider-specific parameters and requirements.

