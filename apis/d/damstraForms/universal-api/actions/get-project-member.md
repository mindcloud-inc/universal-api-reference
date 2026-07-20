# Damstra Forms: Get Project Member

Retrieves a project member from Damstra Forms.

```
GET https://connect.mindcloud.co/v1/universal/damstraForms/latest/actions/get-project-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Damstra Forms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/damstraForms/latest/actions/get-project-member?connectionId=$CONNECTION_ID&projectId=1%20or%20ad03b045-7463-49dd-b50c-be59451bcf1f&userId=1%20or%201acb964c-80c5-412b-ac34-ee6acfde5f1c" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "1 or ad03b045-7463-49dd-b50c-be59451bcf1f",
  "userId": "1 or 1acb964c-80c5-412b-ac34-ee6acfde5f1c"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/damstraForms/latest/actions/get-project-member?${params}`, {
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
| `projectId` | string | yes | The unique id (numeric) or uuid (string) of the project. Example: `1 or ad03b045-7463-49dd-b50c-be59451bcf1f`. |
| `userId` | string | yes | The unique id (numeric) or uuid (string) of the user. Example: `1 or 1acb964c-80c5-412b-ac34-ee6acfde5f1c`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "approverTypeIds": [
        1
      ],
      "canApprove": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "lockVersion": 1,
      "permissionLevel": 1,
      "projectId": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userId": 1,
      "userUuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `approverTypeIds` | array<number> | From Damstra Forms API example response. |
| `canApprove` | boolean | From Damstra Forms API example response. |
| `createdAt` | date | From Damstra Forms API example response. |
| `lockVersion` | number | From Damstra Forms API example response. |
| `permissionLevel` | number | From Damstra Forms API example response. |
| `projectId` | number | From Damstra Forms API example response. |
| `updatedAt` | date | From Damstra Forms API example response. |
| `userId` | number | From Damstra Forms API example response. |
| `userUuid` | string | From Damstra Forms API example response. |

## Native endpoint

Through the native Damstra Forms API, this operation is `GET /projects/{project_id}/project_members/{user_id}` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-member.md) for the provider-specific parameters and requirements.

