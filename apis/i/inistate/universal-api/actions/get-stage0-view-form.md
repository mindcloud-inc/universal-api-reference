# Inistate: Get Stage0 View Form

Retrieves the Stage0 view form from Inistate.

```
GET https://connect.mindcloud.co/v1/universal/inistate/latest/actions/get-stage0-view-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Inistate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/inistate/latest/actions/get-stage0-view-form?connectionId=$CONNECTION_ID&entryId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "entryId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/inistate/latest/actions/get-stage0-view-form?${params}`, {
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
| `entryId` | number | yes | Entry to load into the view form. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "classificationForm": {},
      "complexity": 1,
      "footer": {},
      "formChanges": [
        {}
      ],
      "header": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `classificationForm` | object | Provider form design payload. |
| `complexity` | number | Provider complexity flag. |
| `footer` | object | Form footer metadata including available standards and states. |
| `formChanges` | array<object> | Provider form change list. |
| `header` | object | Form header metadata. |

## Native endpoint

Through the native Inistate API, this operation is `POST /api/activity/form` (base URL `https://api.inistate.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-stage0-view-form.md) for the provider-specific parameters and requirements.

