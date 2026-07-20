# Deftform: Get Submission PDF

Retrieves a submission PDF link from Deftform.

```
GET https://connect.mindcloud.co/v1/universal/deftform/latest/actions/get-submission-pdf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deftform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deftform/latest/actions/get-submission-pdf?connectionId=$CONNECTION_ID&uuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deftform/latest/actions/get-submission-pdf?${params}`, {
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
| `uuid` | string | yes | The submission UUID returned by the List Form Responses action. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pdf_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pdf_url` | string | Generated PDF URL for the submission. |

## Native endpoint

Through the native Deftform API, this operation is `GET /response/:uuid/pdf` (base URL `https://deftform.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-submission-pdf.md) for the provider-specific parameters and requirements.

