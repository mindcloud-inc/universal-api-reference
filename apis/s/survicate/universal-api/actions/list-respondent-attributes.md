# Survicate: List Respondent Attributes

Retrieves attributes for a specific Survicate respondent.

```
GET https://connect.mindcloud.co/v1/universal/survicate/latest/actions/list-respondent-attributes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Survicate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/survicate/latest/actions/list-respondent-attributes?connectionId=$CONNECTION_ID&respondentUuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "respondentUuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/survicate/latest/actions/list-respondent-attributes?${params}`, {
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
| `respondentUuid` | string | yes | The unique UUID of the respondent. |
| `start` | string | no | The attribute identifier used for paginated results. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "name": "Ava Chen",
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `name` | string | Name of the respondent attribute. |
| `value` | string | Value of the respondent attribute. |

## Native endpoint

Through the native Survicate API, this operation is `GET /respondents/:respondent_uuid/attributes` (base URL `https://data-api.survicate.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-respondent-attributes.md) for the provider-specific parameters and requirements.

