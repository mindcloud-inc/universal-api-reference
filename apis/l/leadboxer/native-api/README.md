# Leadboxer: Native API Reference

A consolidated summary of Leadboxer's API configuration and 34 documented operations, with links to official documentation.

- **Official docs:** https://developers.leadboxer.com/docs/intro
- **API base URL:** `https://data.leadboxer.com`

## Authentication

### API Key

Use a LeadBoxer API key from Settings > API Keys. Requests must send the key in the x-api-key header.

### Credentials

- **API Key:** `apiKey` · required · LeadBoxer API key from Settings > API Keys. MindCloud sends this secret in the x-api-key header for every authenticated request.

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://developers.leadboxer.com/docs/authentication-api-keys)

## Endpoints (34 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Custom Tracking Domain](actions/add-custom-tracking-domain.md) | `POST /v1/management/ctd/add` | [docs](https://developers.leadboxer.com/reference/addcustomtrackingdomain) |
| [Add Dataset](actions/add-dataset.md) | `POST /v1/datasets` | [docs](https://developers.leadboxer.com/reference/adddataset) |
| [Add User Dataset](actions/add-user-dataset.md) | `POST /v1/user-datasets` | [docs](https://developers.leadboxer.com/reference/adduserdataset) |
| [Assign Leads](actions/assign-leads.md) | `PUT /v1/management/assign-leads` | [docs](https://developers.leadboxer.com/reference/assignleads) |
| [Create Or Associate User](actions/create-or-associate-user.md) | `POST /v1/users` | [docs](https://developers.leadboxer.com/reference/adduser) |
| [Create Segment](actions/create-segment.md) | `POST /v1/segments` | [docs](https://developers.leadboxer.com/reference/createsegment) |
| [Delete Custom Tracking Domain](actions/delete-custom-tracking-domain.md) | `DELETE /v1/management/ctd/{{datasetId}}` | [docs](https://developers.leadboxer.com/reference/deletecustomtrackingdomain) |
| [Delete Segment](actions/delete-segment.md) | `DELETE /v1/segments/{{segmentId}}` | [docs](https://developers.leadboxer.com/reference/deletesegment) |
| [Delete User](actions/delete-user.md) | `DELETE /v1/users/{{userId}}` | [docs](https://developers.leadboxer.com/reference/removeuser) |
| [Fetch User Datasets](actions/fetch-user-datasets.md) | `GET /v1/user-datasets` | [docs](https://developers.leadboxer.com/reference/getuserdatasets_1) |
| [Get Custom Tracking Domain](actions/get-custom-tracking-domain.md) | `GET /v1/management/ctd/{{datasetId}}` | [docs](https://developers.leadboxer.com/reference/getcustomtrackingdomains) |
| [Get Default Segment Users](actions/get-default-segment-users.md) | `GET /v1/segment/preference` | [docs](https://developers.leadboxer.com/reference/getusersbysegmentidanddatasetid) |
| [Get User Datasets](actions/get-user-datasets.md) | `GET /v1/users/datasets` | [docs](https://developers.leadboxer.com/reference/getuserdatasets) |
| [Lookup Domain](actions/lookup-domain.md) | `GET /v1/domain-lookup` | [docs](https://developers.leadboxer.com/reference/lookupdomain) |
| [Lookup IP Address](actions/lookup-ip-address.md) | `GET /v1/ip-lookup` | [docs](https://developers.leadboxer.com/reference/lookupip) |
| [Remove Dataset](actions/remove-dataset.md) | `DELETE /v1/datasets/{{datasetId}}` | [docs](https://developers.leadboxer.com/reference/removedataset) |
| [Remove Default Segment](actions/remove-default-segment.md) | `DELETE /v1/segment/preference` | [docs](https://developers.leadboxer.com/reference/deletedefaultsegment) |
| [Remove User Dataset](actions/remove-user-dataset.md) | `DELETE /v1/user-datasets` | [docs](https://developers.leadboxer.com/reference/removeuserdataset) |
| [Resend User Invitation](actions/resend-user-invitation.md) | `GET /v1/users/{{userId}}/invite/resend` | [docs](https://developers.leadboxer.com/reference/resendinvite) |
| [Retrieve Lead Details](actions/retrieve-lead-details.md) | `GET /v1/leads/{{leadId}}` | [docs](https://developers.leadboxer.com/reference/leaddetail) |
| [Retrieve Lead Events](actions/retrieve-lead-events.md) | `GET /v1/leads/events` | [docs](https://developers.leadboxer.com/reference/getevents) |
| [Retrieve Lead Sessions](actions/retrieve-lead-sessions.md) | `GET /v1/leads/sessions` | [docs](https://developers.leadboxer.com/reference/getsessions) |
| [Retrieve Leads](actions/retrieve-leads.md) | `GET /v1/leads` | [docs](https://developers.leadboxer.com/reference/users) |
| [Retrieve Leads CSV](actions/retrieve-leads-csv.md) | `GET /v1/leads/export` | [docs](https://developers.leadboxer.com/reference/userscsv) |
| [Retrieve Segments](actions/retrieve-segments.md) | `GET /v1/segments` | [docs](https://developers.leadboxer.com/reference/getsegments) |
| [Save Default Segment](actions/save-default-segment.md) | `PUT /v1/segment/preference` | [docs](https://developers.leadboxer.com/reference/savedefaultsegment) |
| [Update Custom Tracking Domain](actions/update-custom-tracking-domain.md) | `PUT /v1/management/ctd/update` | [docs](https://developers.leadboxer.com/reference/updatedcustomtrackingdomain) |
| [Update Dataset Name](actions/update-dataset-name.md) | `PUT /v1/datasets/{{datasetId}}/name` | [docs](https://developers.leadboxer.com/reference/updatedatasetname) |
| [Update Form Tracking](actions/update-form-tracking.md) | `PUT /v1/datasets/{{datasetId}}/form-tracking` | [docs](https://developers.leadboxer.com/reference/updateformtracking) |
| [Update Lead Tags](actions/update-lead-tags.md) | `PUT /v1/management/lead-tags` | [docs](https://developers.leadboxer.com/reference/updateleadtags) |
| [Update Segment](actions/update-segment.md) | `PUT /v1/segments/{{segmentId}}` | [docs](https://developers.leadboxer.com/reference/updatesegment) |
| [Update Segment User](actions/update-segment-user.md) | `PUT /v1/segments/user` | [docs](https://developers.leadboxer.com/reference/updatesegmentuser) |
| [Update User Name](actions/update-user-name.md) | `PUT /v1/users/{{userId}}/name` | [docs](https://developers.leadboxer.com/reference/updatename) |
| [Validate Custom Tracking Domain](actions/validate-custom-tracking-domain.md) | `POST /v1/management/ctd/validate` | [docs](https://developers.leadboxer.com/reference/validatecustomtrackingdomain) |
