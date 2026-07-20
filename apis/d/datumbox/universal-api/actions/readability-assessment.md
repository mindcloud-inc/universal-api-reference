# Datumbox: Readability Assessment

Assesses a document's readability in Datumbox.

```
GET https://connect.mindcloud.co/v1/universal/datumbox/latest/actions/readability-assessment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Datumbox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datumbox/latest/actions/readability-assessment?connectionId=$CONNECTION_ID&text=Enter%20the%20text%20to%20analyze%20for%20readability." \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "text": "Enter the text to analyze for readability."
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datumbox/latest/actions/readability-assessment?${params}`, {
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
| `text` | string | yes | The clear text to evaluate for readability. Example: `Enter the text to analyze for readability.`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | string | The readability level returned for the submitted text. |
| `status` | number | Datumbox success flag for the operation. |

## Native endpoint

Through the native Datumbox API, this operation is `POST /ReadabilityAssessment.json` (base URL `http://api.datumbox.com/1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/readability-assessment.md) for the provider-specific parameters and requirements.

