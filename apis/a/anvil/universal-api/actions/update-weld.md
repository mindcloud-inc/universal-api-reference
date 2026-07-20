# Anvil: Update Weld

Updates an existing weld in Anvil.

```
PUT https://connect.mindcloud.co/v1/universal/anvil/latest/actions/update-weld
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Anvil `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/anvil/latest/actions/update-weld" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "variables.eid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/anvil/latest/actions/update-weld', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "variables.eid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `variables.eid` | string | yes | Provide EID for Update Weld. |
| `variables.name` | string | no | Provide Name for Update Weld. |
| `variables.slug` | string | no | Provide Slug for Update Weld. |
| `variables.organizationEid` | string | no | Provide Organization EID for Update Weld. |
| `variables.visibility` | string | no | Provide Visibility for Update Weld. |
| `variables.config` | object | no | Provide Config for Update Weld. |
| `variables.configFile` | file | no | Provide Config File for Update Weld. |
| `variables.isArchived` | boolean | no | Provide Is Archived for Update Weld. |
| `variables.expiresAt` | string | no | Provide Expires At for Update Weld. |
| `variables.draftStep` | string | no | Provide Draft Step for Update Weld. |
| `variables.entryForgeId` | number | no | Provide Entry Forge ID for Update Weld. |
| `variables.entryButtonText` | string | no | Provide Entry Button Text for Update Weld. |
| `variables.entryButtonCopyLink` | boolean | no | Provide Entry Button Copy Link for Update Weld. |
| `variables.signatureEmailSubject` | object | no | Provide Signature Email Subject for Update Weld. |
| `variables.signatureEmailBody` | object | no | Provide Signature Email Body for Update Weld. |
| `variables.dataDisplayTitle` | object | no | Provide Data Display Title for Update Weld. |
| `variables.signatureMode` | string | no | Provide Signature Mode for Update Weld. |
| `variables.signatureProvider` | string | no | Provide Signature Provider for Update Weld. |
| `variables.lockedTitleNew` | string | no | Provide Locked Title New for Update Weld. |
| `variables.lockedDescriptionNew` | string | no | Provide Locked Description New for Update Weld. |
| `variables.lockedTitleExisting` | string | no | Provide Locked Title Existing for Update Weld. |
| `variables.lockedDescriptionExisting` | string | no | Provide Locked Description Existing for Update Weld. |
| `variables.expireAfterDaysComplete` | number | no | Provide Expire After Days Complete for Update Weld. |
| `variables.expireAfterDaysStart` | number | no | Provide Expire After Days Start for Update Weld. |
| `variables.planEid` | string | no | Provide Plan EID for Update Weld. |
| `variables.steps` | object | no | Provide Steps for Update Weld. |
| `variables.signatureStepsMode` | string | no | Provide Signature Steps Mode for Update Weld. |
| `variables.versionNumber` | number | no | Provide Version Number for Update Weld. |
| `variables.weldCompleteEmailRecipients` | object | no | Provide Weld Complete Email Recipients for Update Weld. |
| `variables.weldCompleteEmailEnableForTest` | boolean | no | Provide Weld Complete Email Enable For Test for Update Weld. |
| `variables.mergePDFs` | boolean | no | Provide Merge PDFs for Update Weld. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Anvil API returns.

## Native endpoint

Through the native Anvil API, this operation is `POST /` (base URL `https://graphql.useanvil.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-weld.md) for the provider-specific parameters and requirements.

