# Castor EDC: Get Field

Retrieves a field from Castor EDC by ID.

```
GET https://connect.mindcloud.co/v1/universal/castorEDC/latest/actions/get-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Castor EDC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/castorEDC/latest/actions/get-field?connectionId=$CONNECTION_ID&studyId=string&fieldId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "studyId": "string",
  "fieldId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/castorEDC/latest/actions/get-field?${params}`, {
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
| `studyId` | string | yes | The Castor study UUID. |
| `fieldId` | string | yes | The field UUID. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `include` | string | no | Comma-separated list of extra field properties to include. Accepts multiple values in one string, delimited by `,`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Castor EDC API returns.

## Native endpoint

Through the native Castor EDC API, this operation is `GET /study/:study_id/field/:field_id` (base URL `https://us.castoredc.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-field.md) for the provider-specific parameters and requirements.

