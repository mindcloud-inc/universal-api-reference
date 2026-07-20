# National Science Foundation: Get Award Project Outcomes

Retrieves a project outcomes report from National Science Foundation.

```
GET https://connect.mindcloud.co/v1/universal/nationalScienceFoundation/latest/actions/get-award-project-outcomes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a National Science Foundation `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nationalScienceFoundation/latest/actions/get-award-project-outcomes?connectionId=$CONNECTION_ID&id=1052893" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1052893"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nationalScienceFoundation/latest/actions/get-award-project-outcomes?${params}`, {
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
| `id` | string | yes | Award unique identifier whose project outcomes report should be retrieved, such as 1052893. Example: `1052893`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activeAwd": "string",
      "agency": "string",
      "awardeeName": "Ava Chen",
      "estimatedTotalAmt": "string",
      "expDate": "string",
      "histAwd": "string",
      "id": "string",
      "pdPIName": "Ava Chen",
      "projectOutComesReport": "string",
      "startDate": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activeAwd` | string |  |
| `agency` | string |  |
| `awardeeName` | string |  |
| `estimatedTotalAmt` | string |  |
| `expDate` | string |  |
| `histAwd` | string |  |
| `id` | string |  |
| `pdPIName` | string |  |
| `projectOutComesReport` | string |  |
| `startDate` | string |  |
| `title` | string |  |

## Native endpoint

Through the native National Science Foundation API, this operation is `GET /awards/[:id]/projectoutcomes.json` (base URL `https://api.nsf.gov/services/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-award-project-outcomes.md) for the provider-specific parameters and requirements.

