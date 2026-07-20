# Finnish BIS: Get Code List Description

Retrieves code list details from Finnish BIS.

```
GET https://connect.mindcloud.co/v1/universal/finnishBIS/latest/actions/get-code-list-description
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Finnish BIS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/finnishBIS/latest/actions/get-code-list-description?connectionId=$CONNECTION_ID&code=YRMU&lang=en" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "code": "YRMU",
  "lang": "en"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/finnishBIS/latest/actions/get-code-list-description?${params}`, {
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
| `code` | list<string> | yes | PRH code list identifier to retrieve. One of: `KIELI`, `KONK`, `REK`, `REK_KDI`, `SANE`, `SELTILA`, `SELTILA,SANE,KONK`, `STATUS3`, `TLAHDE`, `TLAJI`, `TOIMI`, `TOIMI2`, `TOIMI3`, `TOIMI4`, `VIRANOM`, `YRMU`. Default: `YRMU`. |
| `lang` | list<string> | yes | Language code for the code list description. One of: `en`, `fi`, `sv`. Default: `en`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string | Plain-text tab-separated code-list description returned by PRH. |

## Native endpoint

Through the native Finnish BIS API, this operation is `GET /description` (base URL `https://avoindata.prh.fi/opendata-ytj-api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-code-list-description.md) for the provider-specific parameters and requirements.

