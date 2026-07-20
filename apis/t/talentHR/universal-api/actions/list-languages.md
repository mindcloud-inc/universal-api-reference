# TalentHR: List Languages

Retrieves supported languages from TalentHR.

```
GET https://connect.mindcloud.co/v1/universal/talentHR/latest/actions/list-languages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TalentHR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/talentHR/latest/actions/list-languages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/talentHR/latest/actions/list-languages?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "id": 1,
      "isDisabled": 1,
      "name": "Ava Chen",
      "rtl": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string | Language code. |
| `id` | number | Language ID. |
| `isDisabled` | number | Whether the language is disabled. |
| `name` | string | Language name. |
| `rtl` | number | Whether the language is right-to-left. |

## Native endpoint

Through the native TalentHR API, this operation is `GET /languages` (base URL `https://pubapi.talenthr.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-languages.md) for the provider-specific parameters and requirements.

