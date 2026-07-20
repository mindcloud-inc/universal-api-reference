# Court Drive: Get Case Root Menu by UUID



```
GET https://connect.mindcloud.co/v1/universal/courtDrive/latest/actions/get-case-root-menu-by-uuid
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Court Drive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/courtDrive/latest/actions/get-case-root-menu-by-uuid?connectionId=$CONNECTION_ID&caseUuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "caseUuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/courtDrive/latest/actions/get-case-root-menu-by-uuid?${params}`, {
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
| `caseUuid` | string | yes | CourtAPI case UUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "case": {},
      "links": {},
      "menu": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `case` | object |  |
| `links` | object |  |
| `menu` | object |  |

## Native endpoint

Through the native Court Drive API, this operation is `GET /cases/pacer/by-uuid/{case_uuid}` (base URL `https://v1.courtapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-case-root-menu-by-uuid.md) for the provider-specific parameters and requirements.

