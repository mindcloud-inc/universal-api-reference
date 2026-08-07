# Add Lead Feedback with Google Ads

## Endpoint

- **Method:** `POST`
- **Path:** `v21/customers/:customerId/localServicesLeads/:leadId:provideLeadFeedback`
- **Base URL:** `https://googleads.googleapis.com/`
- **API:** REST
- **Official documentation:** [Add Lead Feedback](https://developers.google.com/google-ads/api/reference/rpc/v21/LocalServicesLeadService/ProvideLeadFeedback)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `surveyAnswer` | body | `list<string>` | no |
| `surveyDissatisfied.otherReasonComment` | body | `string` | no |
| `surveySatisfied.otherReasonComment` | body | `string` | no |
| `surveyDissatisfied` | body | `object` | no |
| `surveyDissatisfied.surveyDissatisfiedReason` | body | `list<string>` | no |
| `surveySatisfied` | body | `object` | no |
| `surveySatisfied.surveySatisfiedReason` | body | `list<string>` | no |
| `customerId` | path | `list` | yes |
| `leadId` | path | `string` | yes |
