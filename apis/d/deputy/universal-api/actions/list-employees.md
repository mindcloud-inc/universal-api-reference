# Deputy: List Employees

Retrieves the employee list from Deputy.

```
GET https://connect.mindcloud.co/v1/universal/deputy/latest/actions/list-employees
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deputy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deputy/latest/actions/list-employees?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deputy/latest/actions/list-employees?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "allowAppraisal": true,
      "company": 1,
      "contact": 1,
      "created": "string",
      "creator": 1,
      "customFieldData": {},
      "customPronouns": {},
      "dateOfBirth": {},
      "displayName": "Ava Chen",
      "DPMetaData": {
        "creatorInfo": {
          "customPronouns": {},
          "displayName": "Ava Chen",
          "employee": 1,
          "employeeProfile": 1,
          "id": 1,
          "photo": "string",
          "pronouns": 1
        },
        "system": "string"
      },
      "emergencyAddress": {},
      "employmentEndComment": {},
      "employmentEndDate": {},
      "employmentEndReason": {},
      "employmentEndSentiment": {},
      "externalLinkId": {},
      "firstName": "Ava",
      "gender": {},
      "higherDuty": {},
      "historyId": 1,
      "id": 1,
      "jobAppId": {},
      "lastName": "Chen",
      "mainAddress": {},
      "modified": "string",
      "onboardingId": {},
      "otherName": {},
      "photo": {},
      "position": "string",
      "postalAddress": {},
      "pronouns": 1,
      "role": 1,
      "salutation": {},
      "startDate": "string",
      "stressProfile": 1,
      "terminationDate": {},
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `allowAppraisal` | boolean |  |
| `company` | number |  |
| `contact` | number |  |
| `created` | string |  |
| `creator` | number |  |
| `customFieldData` | object |  |
| `customPronouns` | object |  |
| `dateOfBirth` | object |  |
| `displayName` | string |  |
| `DPMetaData.creatorInfo.customPronouns` | object |  |
| `DPMetaData.creatorInfo.displayName` | string |  |
| `DPMetaData.creatorInfo.employee` | number |  |
| `DPMetaData.creatorInfo.employeeProfile` | number |  |
| `DPMetaData.creatorInfo.id` | number |  |
| `DPMetaData.creatorInfo.photo` | string |  |
| `DPMetaData.creatorInfo.pronouns` | number |  |
| `DPMetaData.system` | string |  |
| `emergencyAddress` | object |  |
| `employmentEndComment` | object |  |
| `employmentEndDate` | object |  |
| `employmentEndReason` | object |  |
| `employmentEndSentiment` | object |  |
| `externalLinkId` | object |  |
| `firstName` | string |  |
| `gender` | object |  |
| `higherDuty` | object |  |
| `historyId` | number |  |
| `id` | number |  |
| `jobAppId` | object |  |
| `lastName` | string |  |
| `mainAddress` | object |  |
| `modified` | string |  |
| `onboardingId` | object |  |
| `otherName` | object |  |
| `photo` | object |  |
| `position` | string |  |
| `postalAddress` | object |  |
| `pronouns` | number |  |
| `role` | number |  |
| `salutation` | object |  |
| `startDate` | string |  |
| `stressProfile` | number |  |
| `terminationDate` | object |  |
| `userId` | number |  |

## Native endpoint

Through the native Deputy API, this operation is `GET /api/v1/resource/Employee` (base URL `https://{{credentials.endpoint}}.deputy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-employees.md) for the provider-specific parameters and requirements.

