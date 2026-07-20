# Namsor: Split Name

Retrieves first and last name parts from a full name in Namsor.

```
GET https://connect.mindcloud.co/v1/universal/namsor/latest/actions/split-name
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Namsor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/namsor/latest/actions/split-name?connectionId=$CONNECTION_ID&nameFull=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "nameFull": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/namsor/latest/actions/split-name?${params}`, {
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
| `nameFull` | string | yes | Full name input. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "firstLastName": {},
      "id": "string",
      "name": "Ava Chen",
      "nameParserType": "Ava Chen",
      "nameParserTypeAlt": "Ava Chen",
      "score": 1,
      "script": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `firstLastName` | object |  |
| `id` | string |  |
| `name` | string |  |
| `nameParserType` | string |  |
| `nameParserTypeAlt` | string |  |
| `score` | number |  |
| `script` | string |  |

## Native endpoint

Through the native Namsor API, this operation is `GET /api2/json/parseName/:nameFull` (base URL `https://v2.namsor.com/NamSorAPIv2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/split-name.md) for the provider-specific parameters and requirements.

