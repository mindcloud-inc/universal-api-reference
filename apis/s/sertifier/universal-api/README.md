# <img src="https://images.mindcloud.co/apps/icons/id-y6r-rbbnx-logos_1774285006734.png" alt="Sertifier logo" width="28" height="28"> Sertifier: Universal API

Issue, automate, and track digital certificates and badges

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sertifier/latest
- **Category:** Human Resources / Learning (LMS)
- **Actions:** 23
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://sertifier.com
- **Vendor API docs:** https://sertifier.docs.apiary.io

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Test Authentication](actions/test-authentication.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sertifier/latest/actions/test-authentication?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (23)

### Attribute

| Action | Method | Description |
| --- | --- | --- |
| [Add Attribute](actions/add-attribute.md) | POST | Creates a new attribute in Sertifier. |
| [List Attributes](actions/list-attributes.md) | GET | Finds attributes in Sertifier by search filters. |
| [Update Attribute](actions/update-attribute.md) | PUT | Updates an existing attribute in Sertifier. |

### Authentication

| Action | Method | Description |
| --- | --- | --- |
| [Test Authentication](actions/test-authentication.md) | GET | Tests the current authentication setup for Sertifier. |

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Add Campaign](actions/add-campaign.md) | POST | Creates a new campaign in Sertifier. |
| [Delete Campaign](actions/delete-campaign.md) | DELETE | Deletes an existing campaign from Sertifier. |
| [Get Campaign](actions/get-campaign.md) | GET | Retrieves a campaign from a Sertifier workspace. |
| [List Campaigns](actions/list-campaigns.md) | GET | Finds campaigns in Sertifier by search filters. |
| [Schedule Campaign](actions/schedule-campaign.md) | PUT | Schedules an existing campaign in Sertifier. |
| [Send Campaign](actions/send-campaign.md) | PUT | Sends an existing campaign in Sertifier. |
| [Update Campaign](actions/update-campaign.md) | PUT | Updates an existing campaign in Sertifier. |

### Credential

| Action | Method | Description |
| --- | --- | --- |
| [Add Credentials To Campaign](actions/add-credentials-to-campaign.md) | POST | Adds credentials to a Sertifier campaign. |
| [Delete Credential](actions/delete-credential.md) | DELETE | Deletes an existing credential from Sertifier. |
| [Generate Credential PDF Link](actions/generate-credential-pdf-link.md) | GET | Retrieves a credential PDF link from Sertifier. |
| [Get Credential](actions/get-credential.md) | GET | Retrieves a credential from a Sertifier workspace. |
| [List Credentials](actions/list-credentials.md) | GET | Finds credentials in Sertifier by search filters. |
| [Publish Credential](actions/publish-credential.md) | PUT | Publishes an existing credential in Sertifier. |
| [Update Credential](actions/update-credential.md) | PUT | Updates an existing credential in Sertifier. |

### Recipient

| Action | Method | Description |
| --- | --- | --- |
| [Add Recipient](actions/add-recipient.md) | POST | Creates a new recipient in Sertifier. |
| [Delete Recipient](actions/delete-recipient.md) | DELETE | Deletes an existing recipient from Sertifier. |
| [List Recipients](actions/list-recipients.md) | GET | Finds recipients in Sertifier by search filters. |
| [Update Recipient](actions/update-recipient.md) | PUT | Updates an existing recipient in Sertifier. |

### Skill

| Action | Method | Description |
| --- | --- | --- |
| [List Skills](actions/list-skills.md) | GET | Finds skills in Sertifier by search filters. |

