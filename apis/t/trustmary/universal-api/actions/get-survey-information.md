# Trustmary: Get Survey Information

Retrieves survey details from Trustmary.

```
GET https://connect.mindcloud.co/v1/universal/trustmary/latest/actions/get-survey-information
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Trustmary `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trustmary/latest/actions/get-survey-information?connectionId=$CONNECTION_ID&surveyId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "surveyId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trustmary/latest/actions/get-survey-information?${params}`, {
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
| `surveyId` | string | yes | Trustmary survey ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "survey": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `survey` | object | Survey details returned by Trustmary. |

## Native endpoint

Through the native Trustmary API, this operation is `GET /survey/:surveyId` (base URL `https://api.trustmary.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-survey-information.md) for the provider-specific parameters and requirements.

