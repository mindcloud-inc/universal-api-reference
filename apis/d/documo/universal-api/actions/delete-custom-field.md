# Documo: Delete Custom Field

Deletes an existing custom field from Documo.

```
DELETE https://connect.mindcloud.co/v1/universal/documo/latest/actions/delete-custom-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Documo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/documo/latest/actions/delete-custom-field?connectionId=$CONNECTION_ID&customFieldId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customFieldId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/documo/latest/actions/delete-custom-field?${params}`, {
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
| `customFieldId` | string | yes | String \| Required \| Custom Field UUID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customFieldId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customFieldId` | string |  |

## Native endpoint

Through the native Documo API, this operation is `DELETE /v1/custom-fields/:customFieldId` (base URL `https://api.documo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-custom-field.md) for the provider-specific parameters and requirements.

