# <img src="https://images.mindcloud.co/apps/icons/leadboxer-icon_1775156713701.png" alt="Leadboxer logo" width="28" height="28"> Leadboxer: Universal API

LeadBoxer is a lead data platform for lead identification, qualification, website visitor intelligence, and lead management across website, email, and enrichment data.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/leadboxer/latest
- **Actions:** 34
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.leadboxer.com
- **Vendor API docs:** https://developers.leadboxer.com/docs/intro

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Custom Tracking Domain](actions/get-custom-tracking-domain.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leadboxer/latest/actions/get-custom-tracking-domain?connectionId=$CONNECTION_ID&datasetId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (34)

### Dataset

| Action | Method | Description |
| --- | --- | --- |
| [Get Custom Tracking Domain](actions/get-custom-tracking-domain.md) | GET | Retrieves custom tracking domains for a dataset in Leadboxer. |

### Datasets

| Action | Method | Description |
| --- | --- | --- |
| [Add Custom Tracking Domain](actions/add-custom-tracking-domain.md) | POST | Creates a custom tracking domain in Leadboxer and starts certificate generation. |
| [Add Dataset](actions/add-dataset.md) | POST | Creates a new dataset in Leadboxer. |
| [Add User Dataset](actions/add-user-dataset.md) | POST | Creates a user-dataset association in Leadboxer. |
| [Delete Custom Tracking Domain](actions/delete-custom-tracking-domain.md) | DELETE | Deletes a custom tracking domain from a dataset in Leadboxer. |
| [Fetch User Datasets](actions/fetch-user-datasets.md) | GET | Retrieves datasets for a user in Leadboxer. |
| [Get User Datasets](actions/get-user-datasets.md) | GET | Retrieves datasets for the authenticated user in Leadboxer. |
| [Remove Dataset](actions/remove-dataset.md) | DELETE | Deletes an existing dataset from Leadboxer. |
| [Remove User Dataset](actions/remove-user-dataset.md) | DELETE | Deletes a user-dataset association in Leadboxer. |
| [Update Custom Tracking Domain](actions/update-custom-tracking-domain.md) | PUT | Updates a custom tracking domain for a dataset in Leadboxer. |
| [Update Dataset Name](actions/update-dataset-name.md) | PUT | Updates an existing dataset name in Leadboxer. |
| [Update Form Tracking](actions/update-form-tracking.md) | PUT | Updates form tracking settings for a dataset in Leadboxer. |
| [Validate Custom Tracking Domain](actions/validate-custom-tracking-domain.md) | POST | Validates a custom tracking domain in Leadboxer. |

### Events

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Lead Events](actions/retrieve-lead-events.md) | GET | Retrieves lead events in Leadboxer by session ID. |

### Leads

| Action | Method | Description |
| --- | --- | --- |
| [Assign Leads](actions/assign-leads.md) | PUT | Assigns a lead to a user in Leadboxer. |
| [Retrieve Lead Details](actions/retrieve-lead-details.md) | GET | Retrieves lead details from Leadboxer. |
| [Retrieve Leads](actions/retrieve-leads.md) | GET | Retrieves leads from Leadboxer. |
| [Retrieve Leads CSV](actions/retrieve-leads-csv.md) | GET | Retrieves leads as a CSV export from Leadboxer. |
| [Update Lead Tags](actions/update-lead-tags.md) | PUT | Updates lead tags for a lead in Leadboxer. |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [Lookup Domain](actions/lookup-domain.md) | GET | Finds organization details in Leadboxer by domain name. |
| [Lookup IP Address](actions/lookup-ip-address.md) | GET | Finds organization details in Leadboxer by IP address. |

### Segments

| Action | Method | Description |
| --- | --- | --- |
| [Create Segment](actions/create-segment.md) | POST | Creates a new segment in Leadboxer. |
| [Delete Segment](actions/delete-segment.md) | DELETE | Deletes an existing segment from Leadboxer. |
| [Get Default Segment Users](actions/get-default-segment-users.md) | GET | Retrieves user IDs for a default segment in Leadboxer. |
| [Remove Default Segment](actions/remove-default-segment.md) | DELETE | Deletes a user's default segment in Leadboxer. |
| [Retrieve Segments](actions/retrieve-segments.md) | GET | Retrieves segments from Leadboxer. |
| [Save Default Segment](actions/save-default-segment.md) | PUT | Updates default segment assignments for users in Leadboxer. |
| [Update Segment](actions/update-segment.md) | PUT | Updates an existing segment in Leadboxer. |
| [Update Segment User](actions/update-segment-user.md) | PUT | Updates segment access for a user in Leadboxer. |

### Sessions

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Lead Sessions](actions/retrieve-lead-sessions.md) | GET | Retrieves lead sessions in Leadboxer by lead ID. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Create Or Associate User](actions/create-or-associate-user.md) | POST | Creates a user in Leadboxer, or associates an existing one. |
| [Delete User](actions/delete-user.md) | DELETE | Deletes an existing user from Leadboxer. |
| [Resend User Invitation](actions/resend-user-invitation.md) | GET | Resends a user invitation in Leadboxer. |
| [Update User Name](actions/update-user-name.md) | PUT | Updates an existing user's name in Leadboxer. |

