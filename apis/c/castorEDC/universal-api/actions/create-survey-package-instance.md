# Castor EDC: Create Survey Package Instance

Creates a survey package instance in Castor EDC.

```
POST https://connect.mindcloud.co/v1/universal/castorEDC/latest/actions/create-survey-package-instance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Castor EDC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/castorEDC/latest/actions/create-survey-package-instance" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "studyId": "string",
  "surveyPackageId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/castorEDC/latest/actions/create-survey-package-instance', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "studyId": "string",
    "surveyPackageId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `studyId` | string | yes | The Castor study UUID. |
| `surveyPackageId` | string | yes | The survey package UUID to instantiate. |
| `participantId` | string | no | Participant UUID to receive the survey package instance. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ccrPatientId` | string | no | CCR patient identifier to receive the survey package instance. |
| `emailAddress` | string | no | Optional email address to send the invitation to. |
| `packageInvitationSubject` | string | no | Optional subject for the invitation email. |
| `packageInvitation` | string | no | Optional invitation email body; include {url} if you want Castor to send it from this request. |
| `availableFrom` | string | no | UTC datetime when the survey package instance becomes available or is scheduled to send. |
| `autoLockOnFinish` | boolean | no | Lock the survey package instance automatically when the respondent finishes. |
| `parentType` | string | no | Parent type: 0 none, 1 visit, 2 repeating data instance. |
| `parentId` | string | no | Optional UUID of the parent visit or repeating data instance. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Castor EDC API returns.

## Native endpoint

Through the native Castor EDC API, this operation is `POST /study/:study_id/survey-package-instance` (base URL `https://us.castoredc.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-survey-package-instance.md) for the provider-specific parameters and requirements.

