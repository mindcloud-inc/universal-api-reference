# Invite Candidates Via Email with TestDome

Invites candidates via email in TestDome.

## Endpoint

- **Method:** `POST`
- **Path:** `/tests/:testId/candidates/invite-via-email`
- **Base URL:** `https://api.staging.testdome.com/v3`
- **Official documentation:** [Invite Candidates Via Email](https://api.testdome.com/openapi-ui/index/index.html?urls.primaryName=v3%20Docs)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `body` | body | `string` | yes |
| `deadline` | body | `string` | yes |
| `emails` | body | `list<string>` | yes |
| `id` | path | `number` | yes |
| `proctoringEnabled` | body | `boolean` | yes |
| `replyTo` | body | `string` | yes |
