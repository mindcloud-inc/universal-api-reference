# Add Credentials To Campaign with Sertifier

Adds credentials to a Sertifier campaign.

## Endpoint

- **Method:** `POST`
- **Path:** `/campaign/addCredentials`
- **Base URL:** `https://b2b.sertifier.com`
- **Official documentation:** [Add Credentials To Campaign](https://sertifier.docs.apiary.io/reference/campaign/add-credentials)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `credentials[].campaignId` | body | `string` | yes |
| `credentials[].name` | body | `string` | yes |
| `credentials[].email` | body | `string` | no |
| `credentials[].issueDate` | body | `date` | no |
| `credentials[].expireDate` | body | `date` | no |
| `credentials[].quickPublish` | body | `boolean` | no |
| `credentials[].externalId` | body | `string` | no |
| `credentials[].dontSendEmail` | body | `boolean` | no |
