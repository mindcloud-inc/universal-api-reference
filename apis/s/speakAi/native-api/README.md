# Speak Ai: Native API Reference

A consolidated summary of Speak Ai's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://docs.speakai.co/
- **API base URL:** `https://api.speakai.co/v1`

## Authentication

### API Key + Session Token

Connect with your Speak Ai API key. Most provider endpoints also require a short-lived session access token that you mint from that key using the Request Access Token action.

### Credentials

- **API Key:** `apiKey` · required · Speak Ai API key from Developers > API Keys.
- **Access Token:** `accessToken` · optional · Temporary Speak Ai session access token returned by the Request Access Token action. Leave blank until you mint one.
- **Refresh Token:** `refreshToken` · optional · Temporary Speak Ai session refresh token returned by the Request Access Token action for reference and future re-auth work.

Send these headers with each API request:

```http
x-speakai-key: <apiKey>
x-access-token: <accessToken>
```

[Official authentication documentation](https://help.speakai.co/en/articles/6150141-how-to-get-your-api-key)

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Folder](actions/create-folder.md) | `POST /folder` | [docs](https://docs.speakai.co/#4022c583-e3ef-4615-b181-083c6ccc1272) |
| [Create Recorder](actions/create-recorder.md) | `POST /recorder/create` | [docs](https://docs.speakai.co/#0e1a7b2c-9e8b-4a22-8560-d6f95a86f124) |
| [Create Text Note](actions/create-text-note.md) | `POST /text/create` | [docs](https://docs.speakai.co/#1001bb40-bc9c-42f8-ad2d-03c5cf131cb6) |
| [Delete Folder](actions/delete-folder.md) | `DELETE /folder/:folderId` | [docs](https://docs.speakai.co/#837cd417-49be-4af0-9249-bfc417ae1a40) |
| [Delete Media](actions/delete-media.md) | `DELETE /media/:mediaId` | [docs](https://docs.speakai.co/#e7f7950f-6f2d-4d36-88d6-d65fc694151a) |
| [Delete Text Note](actions/delete-text-note.md) | `DELETE /text/:mediaId` | [docs](https://docs.speakai.co/#3f934551-d437-4d80-9041-cd6b348ae92e) |
| [Export Content](actions/export-content.md) | `POST /:mediaType/export/:mediaId/:fileType` | [docs](https://docs.speakai.co/#fcdaa5ed-cd17-48ba-98c7-2a7af4e13ce6) |
| [Get Folder](actions/get-folder.md) | `GET /folder/:folderId` | [docs](https://docs.speakai.co/#f8daf40d-c996-46ca-8767-ec49e68bf0a4) |
| [Get Media Insight](actions/get-media-insight.md) | `GET /media/insight/:mediaId` | [docs](https://docs.speakai.co/#0b586e5b-6e0a-4b79-b440-e6889a803ccd) |
| [Get Media Status](actions/get-media-status.md) | `GET /media/status/:mediaId` | [docs](https://docs.speakai.co/#c4bb2b6b-cd0a-44ec-9afb-9e253bcfeff1) |
| [Get Media Transcript](actions/get-media-transcript.md) | `GET /media/transcript/:mediaId` | [docs](https://docs.speakai.co/#1bb23cc2-457d-4798-b914-e85b94a9289c) |
| [Get Recorder](actions/get-recorder.md) | `GET /recorder/:recorderId` | [docs](https://docs.speakai.co/#9de4ec29-7bcc-438c-96e5-f8a7f7566b74) |
| [Get Text Insight](actions/get-text-insight.md) | `GET /text/insight/:mediaId` | [docs](https://docs.speakai.co/#d65573c9-98ad-4089-93ad-9d0a173fdeea) |
| [Get Upload Signed URL](actions/get-upload-signed-url.md) | `GET /media/upload/signedurl` | [docs](https://docs.speakai.co/#24bd40af-fdb6-42e3-a89b-e55f7670db16) |
| [List Folders](actions/list-folders.md) | `GET /folder` | [docs](https://docs.speakai.co/#718b2911-1f76-40c8-8c21-8782ce357871) |
| [List Media](actions/list-media.md) | `GET /media` | [docs](https://docs.speakai.co/#8f14b0e6-7d40-40eb-8ea7-328943326e3b) |
| [List Recorders](actions/list-recorders.md) | `GET /recorder` | [docs](https://docs.speakai.co/#cfd4b7ea-0b58-4719-b5a9-213954d1da44) |
| [Reanalyze Text](actions/reanalyze-text.md) | `GET /media/reanalyze/:mediaId` | [docs](https://docs.speakai.co/) |
| [Request Access Token](actions/request-access-token.md) | `POST /auth/accessToken` | [docs](https://docs.speakai.co/#d6e01d83-dff8-4b05-b282-2627feac9525) |
| [Update Folder](actions/update-folder.md) | `PUT /folder/:folderId` | [docs](https://docs.speakai.co/#c69a7f0e-1a72-4b5a-b56f-014a6b285113) |
| [Update Media](actions/update-media.md) | `PUT /media/:mediaId` | [docs](https://docs.speakai.co/#ac30a062-e214-4771-b131-afeda3b5320e) |
| [Update Media Speakers](actions/update-media-speakers.md) | `PUT /media/speakers/:mediaId` | [docs](https://docs.speakai.co/#eacfa313-5bb9-47b7-ad8b-ae730b89de5a) |
| [Update Text Note](actions/update-text-note.md) | `PUT /text/update/:mediaId` | [docs](https://docs.speakai.co/#dd13ff94-db3b-47b3-9120-51f9929abc5e) |
| [Upload Media](actions/upload-media.md) | `POST /media/upload` | [docs](https://docs.speakai.co/#c6106a66-6a3d-4b05-b4a2-4a68a4c1e95d) |
