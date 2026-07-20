# <img src="https://images.mindcloud.co/apps/icons/images-7_1775150492795.png" alt="ONLYOFFICE DocSpace logo" width="28" height="28"> ONLYOFFICE DocSpace: Universal API

Store, manage, and collaborate on documents in customizable rooms

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/oNLYOFFICEDocSpace/latest
- **Category:** Content & Files / Storage
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.onlyoffice.com/docspace.aspx
- **Vendor API docs:** https://api.onlyoffice.com/docspace/api-backend/usage-api/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get My Profile](actions/get-my-profile.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oNLYOFFICEDocSpace/latest/actions/get-my-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

### File

| Action | Method | Description |
| --- | --- | --- |
| [Get File Settings](actions/get-file-settings.md) | GET | Retrieves file settings from ONLYOFFICE DocSpace. |

### Folder

| Action | Method | Description |
| --- | --- | --- |
| [Get My Documents Section](actions/get-my-documents-section.md) | GET | Retrieves your My Documents section from ONLYOFFICE DocSpace. |

### Portal

| Action | Method | Description |
| --- | --- | --- |
| [Get Portal Capabilities](actions/get-portal-capabilities.md) | GET | Retrieves portal capabilities from ONLYOFFICE DocSpace. |
| [Get Portal Information](actions/get-portal-information.md) | GET | Retrieves portal information from ONLYOFFICE DocSpace. |
| [Get Portal Settings](actions/get-portal-settings.md) | GET | Retrieves portal settings from ONLYOFFICE DocSpace. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get My Profile](actions/get-my-profile.md) | GET | Retrieves your profile from ONLYOFFICE DocSpace. |

