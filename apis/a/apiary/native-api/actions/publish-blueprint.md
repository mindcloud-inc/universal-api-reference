# Publish Blueprint with Apiary

Publishes an API blueprint in Apiary.

## Endpoint

- **Method:** `POST`
- **Path:** `/blueprint/publish/{{apiName}}`
- **Base URL:** `https://api.apiary.io`
- **Official documentation:** [Publish Blueprint](https://apiary.docs.apiary.io/reference/publish-blueprint)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `apiName` | path | `string` | yes | Select the Apiary API subdomain to publish blueprint source to. |
| `code` | body | `string` | yes | Full API Blueprint source to publish. |
| `messageToSave` | body | `string` | no | Commit message shown in Apiary history. |
| `shouldCommit` | body | `string` | yes | Apiary publish flag. Use `yes` to commit or `no` for the current publish behavior. Accepted values: `0`, `1`. |
