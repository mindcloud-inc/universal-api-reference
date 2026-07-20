# Startquestion: Get Respondent Patch

Retrieves a Startquestion respondent patch by ID.

```
GET https://connect.mindcloud.co/v1/universal/startquestion/latest/actions/get-respondent-patch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Startquestion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/startquestion/latest/actions/get-respondent-patch?connectionId=$CONNECTION_ID&patchId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "patchId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/startquestion/latest/actions/get-respondent-patch?${params}`, {
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
| `patchId` | string | yes | Patch ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "respondents": [
        1
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `respondents` | array<number> | Respondent IDs created in the patch. |

## Native endpoint

Through the native Startquestion API, this operation is `GET /respondents/patch` (base URL `https://www.startquestion.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-respondent-patch.md) for the provider-specific parameters and requirements.

