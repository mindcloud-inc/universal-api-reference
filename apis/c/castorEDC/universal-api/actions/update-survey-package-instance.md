# Castor EDC: Update Survey Package Instance

Updates a survey package instance in Castor EDC.

```
PUT https://connect.mindcloud.co/v1/universal/castorEDC/latest/actions/update-survey-package-instance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Castor EDC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/castorEDC/latest/actions/update-survey-package-instance" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "studyId": "string",
  "surveyPackageInstanceId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/castorEDC/latest/actions/update-survey-package-instance', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "studyId": "string",
    "surveyPackageInstanceId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `studyId` | string | yes | The Castor study UUID. |
| `surveyPackageInstanceId` | string | yes | The survey package instance UUID. |
| `locked` | boolean | no | Lock or unlock the survey package instance. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sentOn` | string | no | UTC datetime when the survey package instance was sent. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Castor EDC API returns.

## Native endpoint

Through the native Castor EDC API, this operation is `PATCH /study/:study_id/survey-package-instance/:survey_package_instance_id` (base URL `https://us.castoredc.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-survey-package-instance.md) for the provider-specific parameters and requirements.

