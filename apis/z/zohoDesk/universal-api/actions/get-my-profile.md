# Zoho Desk: Get My Profile

Retrieve the configuration details and permissions defined for the profile of the currently logged in user.

```
GET https://connect.mindcloud.co/v1/universal/zohoDesk/latest/actions/get-my-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Desk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoDesk/latest/actions/get-my-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoDesk/latest/actions/get-my-profile?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "default": true,
      "description": "string",
      "id": 1,
      "isVisible": true,
      "name": "Ava Chen",
      "permissions": {
        "accounts": {
          "create": true,
          "delete": true,
          "deleteSharedCustomViews": true,
          "edit": true,
          "editSharedCustomViews": true,
          "export": true,
          "import": true,
          "manageOwnCustomViews": true,
          "reshareSharedCustomViews": true,
          "shareOwnCustomViews": true,
          "view": true
        },
        "activities": {
          "deleteSharedCustomViews": true,
          "editSharedCustomViews": true,
          "manageOwnCustomViews": true,
          "reshareSharedCustomViews": true,
          "shareOwnCustomViews": true
        },
        "agents": {
          "create": true,
          "delete": true,
          "edit": true,
          "import": true,
          "overview": true,
          "viewAllFields": true
        },
        "calls": {
          "create": true,
          "delete": true,
          "deleteSharedCustomViews": true,
          "edit": true,
          "editSharedCustomViews": true,
          "export": true,
          "import": true,
          "manageOwnCustomViews": true,
          "reshareSharedCustomViews": true,
          "shareOwnCustomViews": true,
          "view": true
        },
        "chat": {
          "view": true
        },
        "clientAction": {
          "create": true,
          "delete": true,
          "deleteSharedCustomViews": true,
          "edit": true,
          "editSharedCustomViews": true,
          "export": true,
          "manageOwnCustomViews": true,
          "reshareSharedCustomViews": true,
          "shareOwnCustomViews": true,
          "view": true
        },
        "clientActionConditions": {
          "create": true,
          "delete": true,
          "deleteSharedCustomViews": true,
          "edit": true,
          "editSharedCustomViews": true,
          "export": true,
          "manageOwnCustomViews": true,
          "reshareSharedCustomViews": true,
          "shareOwnCustomViews": true,
          "view": true
        },
        "clientActionLocationAssociation": {
          "create": true,
          "delete": true,
          "deleteSharedCustomViews": true,
          "edit": true,
          "editSharedCustomViews": true,
          "export": true,
          "manageOwnCustomViews": true,
          "reshareSharedCustomViews": true,
          "shareOwnCustomViews": true,
          "view": true
        },
        "clientActionModuleAssociation": {
          "create": true,
          "delete": true,
          "deleteSharedCustomViews": true,
          "edit": true,
          "editSharedCustomViews": true,
          "export": true,
          "manageOwnCustomViews": true,
          "reshareSharedCustomViews": true,
          "shareOwnCustomViews": true,
          "view": true
        },
        "clientEvents": {
          "create": true,
          "delete": true,
          "deleteSharedCustomViews": true,
          "edit": true,
          "editSharedCustomViews": true,
          "export": true,
          "manageOwnCustomViews": true,
          "reshareSharedCustomViews": true,
          "shareOwnCustomViews": true,
          "view": true
        },
        "comments": {
          "delete": true,
          "deleteOthers": true,
          "edit": true,
          "editOthers": true
        },
        "community": {
          "create": true,
          "delete": true,
          "edit": true,
          "moderate": true,
          "view": true
        },
        "communityComment": {
          "view": true
        },
        "communityTopic": {
          "view": true
        },
        "componentEventMappingAssociation": {
          "create": true,
          "delete": true,
          "deleteSharedCustomViews": true,
          "edit": true,
          "editSharedCustomViews": true,
          "export": true,
          "manageOwnCustomViews": true,
          "reshareSharedCustomViews": true,
          "shareOwnCustomViews": true,
          "view": true
        },
        "componentMapping": {
          "create": true,
          "delete": true,
          "deleteSharedCustomViews": true,
          "edit": true,
          "editSharedCustomViews": true,
          "export": true,
          "manageOwnCustomViews": true,
          "reshareSharedCustomViews": true,
          "shareOwnCustomViews": true,
          "view": true
        },
        "contacts": {
          "create": true,
          "delete": true,
          "deleteSharedCustomViews": true,
          "edit": true,
          "editSharedCustomViews": true,
          "export": true,
          "import": true,
          "manageOwnCustomViews": true,
          "reshareSharedCustomViews": true,
          "shareOwnCustomViews": true,
          "view": true
        },
        "contracts": {
          "create": true,
          "delete": true,
          "deleteSharedCustomViews": true,
          "edit": true,
          "editSharedCustomViews": true,
          "export": true,
          "import": true,
          "manageOwnCustomViews": true,
          "reshareSharedCustomViews": true,
          "shareOwnCustomViews": true,
          "view": true
        },
        "courses": {
          "create": true,
          "delete": true,
          "deleteSharedCustomViews": true,
          "edit": true,
          "editSharedCustomViews": true,
          "export": true,
          "manageOwnCustomViews": true,
          "reshareSharedCustomViews": true,
          "shareOwnCustomViews": true,
          "view": true
        },
        "crmInteg": {
          "crmAccountsActivityCalls": true,
          "crmAccountsActivityEvents": true,
          "crmAccountsActivityTasks": true,
          "crmAccountsInfo": true,
          "crmAccountsNotes": true,
          "crmAccountsPotentials": true,
          "crmContactsActivityCalls": true,
          "crmContactsActivityEvents": true,
          "crmContactsActivityTasks": true,
          "crmContactsInfo": true,
          "crmContactsNotes": true,
          "crmContactsPotentials": true
        },
        "eventMapping": {
          "create": true,
          "delete": true,
          "deleteSharedCustomViews": true,
          "edit": true,
          "editSharedCustomViews": true,
          "export": true,
          "manageOwnCustomViews": true,
          "reshareSharedCustomViews": true,
          "shareOwnCustomViews": true,
          "view": true
        },
        "events": {
          "create": true,
          "delete": true,
          "deleteSharedCustomViews": true,
          "edit": true,
          "editSharedCustomViews": true,
          "export": true,
          "import": true,
          "manageOwnCustomViews": true,
          "reshareSharedCustomViews": true,
          "shareOwnCustomViews": true,
          "view": true
        },
        "financeInteg": {
          "createContact": true,
          "createEstimate": true,
          "createInvoice": true,
          "createSalesOrder": true,
          "sendEstimate": true,
          "sendInvoice": true,
          "sendSalesOrder": true,
          "viewEstimate": true,
          "viewInvoice": true,
          "viewSalesOrder": true,
          "viewSubscription": true
        },
        "gc": {
          "create": true,
          "delete": true,
          "edit": true,
          "view": true
        },
        "im": {
          "create": true,
          "delete": true,
          "edit": true,
          "view": true
        },
        "imConversations": {
          "create": true,
          "delete": true,
          "deleteSharedCustomViews": true,
          "edit": true,
          "editSharedCustomViews": true,
          "export": true,
          "manageOwnCustomViews": true,
          "reshareSharedCustomViews": true,
          "shareOwnCustomViews": true,
          "view": true
        },
        "imMessages": {
          "create": true,
          "delete": true,
          "deleteSharedCustomViews": true,
          "edit": true,
          "editSharedCustomViews": true,
          "export": true,
          "manageOwnCustomViews": true,
          "reshareSharedCustomViews": true,
          "shareOwnCustomViews": true,
          "view": true
        },
        "kbCategory": {
          "admin": true,
          "create": true,
          "delete": true,
          "edit": true,
          "editAllArticles": true,
          "export": true,
          "import": true,
          "manageKB": true,
          "view": true
        },
        "managerDashboard": {
          "allView": true,
          "customize": true,
          "myView": true
        },
        "mobileapp": {
          "customMobileApps": true,
          "deskapp": true,
          "radar": true
        },
        "modules": {
          "create": true,
          "delete": true,
          "deleteSharedCustomViews": true,
          "edit": true,
          "editSharedCustomViews": true,
          "export": true,
          "manageOwnCustomViews": true,
          "reshareSharedCustomViews": true,
          "shareOwnCustomViews": true,
          "view": true
        },
        "products": {
          "create": true,
          "delete": true,
          "deleteSharedCustomViews": true,
          "edit": true,
          "editSharedCustomViews": true,
          "export": true,
          "import": true,
          "manageOwnCustomViews": true,
          "reshareSharedCustomViews": true,
          "shareOwnCustomViews": true,
          "view": true
        },
        "radar": {
          "activities": true,
          "agentStats": true,
          "apiUsageAlerts": true,
          "auditLog": true,
          "averageHandlingTime": true,
          "channelTraffic": true,
          "contacts": true,
          "currentStats": true,
          "customerHappiness": true,
          "dailyToast": true,
          "dailyTrend": true,
          "dashboards": true,
          "exceptionHandling": true,
          "fcr": true,
          "feeds": true,
          "im": true,
          "kb": true,
          "liveTraffic": true,
          "manageRadar": true,
          "mostThreadedTickets": true,
          "quickView": true,
          "textContentProtection": true,
          "visualContentProtection": true
        },
        "reports": {
          "create": true,
          "delete": true,
          "edit": true,
          "export": true,
          "view": true
        },
        "setup": {
          "automation": true,
          "buttons": true,
          "chat": true,
          "community": true,
          "customerHappiness": true,
          "department": true,
          "email": true,
          "exportPortalUsers": true,
          "exportUsers": true,
          "featureConfig": true,
          "fetchAcrossDepartment": true,
          "gamification": true,
          "globalReports": true,
          "googleAnalytics": true,
          "im": true,
          "importHistory": true,
          "layouts": true,
          "localization": true,
          "manageAgents": true,
          "manageMarketplace": true,
          "managerDashboard": true,
          "massComment": true,
          "massReply": true,
          "moveRecords": true,
          "permission": true,
          "pinnedConversations": true,
          "portal": true,
          "portalUsers": true,
          "privacySettings": true,
          "rebranding": true,
          "recycleBin": true,
          "sandbox": true,
          "securitySettings": true,
          "shareSnippet": true,
          "signUpApproval": true,
          "social": true,
          "tabsAndFields": true,
          "teams": true,
          "telephony": true,
          "templates": true,
          "timeTracking": true,
          "webForm": true,
          "webhooks": true
        },
        "social": {
          "twitterConversationReply": true,
          "twitterPostCreate": true,
          "twitterPostDelete": true,
          "view": true
        },
        "supportEmailAddress": {
          "create": true,
          "delete": true,
          "deleteSharedCustomViews": true,
          "edit": true,
          "editSharedCustomViews": true,
          "export": true,
          "manageOwnCustomViews": true,
          "reshareSharedCustomViews": true,
          "shareOwnCustomViews": true,
          "view": true
        },
        "tasks": {
          "create": true,
          "delete": true,
          "deleteSharedCustomViews": true,
          "edit": true,
          "editSharedCustomViews": true,
          "export": true,
          "import": true,
          "manageOwnCustomViews": true,
          "reshareSharedCustomViews": true,
          "shareOwnCustomViews": true,
          "view": true
        },
        "ticketLifeCycleData": {
          "create": true,
          "delete": true,
          "deleteSharedCustomViews": true,
          "edit": true,
          "editSharedCustomViews": true,
          "export": true,
          "manageOwnCustomViews": true,
          "reshareSharedCustomViews": true,
          "shareOwnCustomViews": true,
          "view": true
        },
        "tickets": {
          "addFollowers": true,
          "changeOwner": true,
          "closeTicket": true,
          "create": true,
          "delete": true,
          "deleteSharedCustomViews": true,
          "deleteTags": true,
          "edit": true,
          "editSharedCustomViews": true,
          "editTags": true,
          "export": true,
          "handleUnassigned": true,
          "import": true,
          "mailReview": true,
          "mailSend": true,
          "manageOwnCustomViews": true,
          "mergeTickets": true,
          "reshareSharedCustomViews": true,
          "revokeBlueprint": true,
          "shareOwnCustomViews": true,
          "shareTickets": true,
          "unassignedChangeOwner": true,
          "view": true
        },
        "timeEntry": {
          "create": true,
          "delete": true,
          "edit": true,
          "view": true
        },
        "zia": {
          "create": true,
          "delete": true,
          "edit": true,
          "view": true
        }
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `default` | boolean |  |
| `description` | string |  |
| `id` | number |  |
| `isVisible` | boolean |  |
| `name` | string |  |
| `permissions.accounts.create` | boolean |  |
| `permissions.accounts.delete` | boolean |  |
| `permissions.accounts.deleteSharedCustomViews` | boolean |  |
| `permissions.accounts.edit` | boolean |  |
| `permissions.accounts.editSharedCustomViews` | boolean |  |
| `permissions.accounts.export` | boolean |  |
| `permissions.accounts.import` | boolean |  |
| `permissions.accounts.manageOwnCustomViews` | boolean |  |
| `permissions.accounts.reshareSharedCustomViews` | boolean |  |
| `permissions.accounts.shareOwnCustomViews` | boolean |  |
| `permissions.accounts.view` | boolean |  |
| `permissions.activities.deleteSharedCustomViews` | boolean |  |
| `permissions.activities.editSharedCustomViews` | boolean |  |
| `permissions.activities.manageOwnCustomViews` | boolean |  |
| `permissions.activities.reshareSharedCustomViews` | boolean |  |
| `permissions.activities.shareOwnCustomViews` | boolean |  |
| `permissions.agents.create` | boolean |  |
| `permissions.agents.delete` | boolean |  |
| `permissions.agents.edit` | boolean |  |
| `permissions.agents.import` | boolean |  |
| `permissions.agents.overview` | boolean |  |
| `permissions.agents.viewAllFields` | boolean |  |
| `permissions.calls.create` | boolean |  |
| `permissions.calls.delete` | boolean |  |
| `permissions.calls.deleteSharedCustomViews` | boolean |  |
| `permissions.calls.edit` | boolean |  |
| `permissions.calls.editSharedCustomViews` | boolean |  |
| `permissions.calls.export` | boolean |  |
| `permissions.calls.import` | boolean |  |
| `permissions.calls.manageOwnCustomViews` | boolean |  |
| `permissions.calls.reshareSharedCustomViews` | boolean |  |
| `permissions.calls.shareOwnCustomViews` | boolean |  |
| `permissions.calls.view` | boolean |  |
| `permissions.chat.view` | boolean |  |
| `permissions.clientAction.create` | boolean |  |
| `permissions.clientAction.delete` | boolean |  |
| `permissions.clientAction.deleteSharedCustomViews` | boolean |  |
| `permissions.clientAction.edit` | boolean |  |
| `permissions.clientAction.editSharedCustomViews` | boolean |  |
| `permissions.clientAction.export` | boolean |  |
| `permissions.clientAction.manageOwnCustomViews` | boolean |  |
| `permissions.clientAction.reshareSharedCustomViews` | boolean |  |
| `permissions.clientAction.shareOwnCustomViews` | boolean |  |
| `permissions.clientAction.view` | boolean |  |
| `permissions.clientActionConditions.create` | boolean |  |
| `permissions.clientActionConditions.delete` | boolean |  |
| `permissions.clientActionConditions.deleteSharedCustomViews` | boolean |  |
| `permissions.clientActionConditions.edit` | boolean |  |
| `permissions.clientActionConditions.editSharedCustomViews` | boolean |  |
| `permissions.clientActionConditions.export` | boolean |  |
| `permissions.clientActionConditions.manageOwnCustomViews` | boolean |  |
| `permissions.clientActionConditions.reshareSharedCustomViews` | boolean |  |
| `permissions.clientActionConditions.shareOwnCustomViews` | boolean |  |
| `permissions.clientActionConditions.view` | boolean |  |
| `permissions.clientActionLocationAssociation.create` | boolean |  |
| `permissions.clientActionLocationAssociation.delete` | boolean |  |
| `permissions.clientActionLocationAssociation.deleteSharedCustomViews` | boolean |  |
| `permissions.clientActionLocationAssociation.edit` | boolean |  |
| `permissions.clientActionLocationAssociation.editSharedCustomViews` | boolean |  |
| `permissions.clientActionLocationAssociation.export` | boolean |  |
| `permissions.clientActionLocationAssociation.manageOwnCustomViews` | boolean |  |
| `permissions.clientActionLocationAssociation.reshareSharedCustomViews` | boolean |  |
| `permissions.clientActionLocationAssociation.shareOwnCustomViews` | boolean |  |
| `permissions.clientActionLocationAssociation.view` | boolean |  |
| `permissions.clientActionModuleAssociation.create` | boolean |  |
| `permissions.clientActionModuleAssociation.delete` | boolean |  |
| `permissions.clientActionModuleAssociation.deleteSharedCustomViews` | boolean |  |
| `permissions.clientActionModuleAssociation.edit` | boolean |  |
| `permissions.clientActionModuleAssociation.editSharedCustomViews` | boolean |  |
| `permissions.clientActionModuleAssociation.export` | boolean |  |
| `permissions.clientActionModuleAssociation.manageOwnCustomViews` | boolean |  |
| `permissions.clientActionModuleAssociation.reshareSharedCustomViews` | boolean |  |
| `permissions.clientActionModuleAssociation.shareOwnCustomViews` | boolean |  |
| `permissions.clientActionModuleAssociation.view` | boolean |  |
| `permissions.clientEvents.create` | boolean |  |
| `permissions.clientEvents.delete` | boolean |  |
| `permissions.clientEvents.deleteSharedCustomViews` | boolean |  |
| `permissions.clientEvents.edit` | boolean |  |
| `permissions.clientEvents.editSharedCustomViews` | boolean |  |
| `permissions.clientEvents.export` | boolean |  |
| `permissions.clientEvents.manageOwnCustomViews` | boolean |  |
| `permissions.clientEvents.reshareSharedCustomViews` | boolean |  |
| `permissions.clientEvents.shareOwnCustomViews` | boolean |  |
| `permissions.clientEvents.view` | boolean |  |
| `permissions.comments.delete` | boolean |  |
| `permissions.comments.deleteOthers` | boolean |  |
| `permissions.comments.edit` | boolean |  |
| `permissions.comments.editOthers` | boolean |  |
| `permissions.community.create` | boolean |  |
| `permissions.community.delete` | boolean |  |
| `permissions.community.edit` | boolean |  |
| `permissions.community.moderate` | boolean |  |
| `permissions.community.view` | boolean |  |
| `permissions.communityComment.view` | boolean |  |
| `permissions.communityTopic.view` | boolean |  |
| `permissions.componentEventMappingAssociation.create` | boolean |  |
| `permissions.componentEventMappingAssociation.delete` | boolean |  |
| `permissions.componentEventMappingAssociation.deleteSharedCustomViews` | boolean |  |
| `permissions.componentEventMappingAssociation.edit` | boolean |  |
| `permissions.componentEventMappingAssociation.editSharedCustomViews` | boolean |  |
| `permissions.componentEventMappingAssociation.export` | boolean |  |
| `permissions.componentEventMappingAssociation.manageOwnCustomViews` | boolean |  |
| `permissions.componentEventMappingAssociation.reshareSharedCustomViews` | boolean |  |
| `permissions.componentEventMappingAssociation.shareOwnCustomViews` | boolean |  |
| `permissions.componentEventMappingAssociation.view` | boolean |  |
| `permissions.componentMapping.create` | boolean |  |
| `permissions.componentMapping.delete` | boolean |  |
| `permissions.componentMapping.deleteSharedCustomViews` | boolean |  |
| `permissions.componentMapping.edit` | boolean |  |
| `permissions.componentMapping.editSharedCustomViews` | boolean |  |
| `permissions.componentMapping.export` | boolean |  |
| `permissions.componentMapping.manageOwnCustomViews` | boolean |  |
| `permissions.componentMapping.reshareSharedCustomViews` | boolean |  |
| `permissions.componentMapping.shareOwnCustomViews` | boolean |  |
| `permissions.componentMapping.view` | boolean |  |
| `permissions.contacts.create` | boolean |  |
| `permissions.contacts.delete` | boolean |  |
| `permissions.contacts.deleteSharedCustomViews` | boolean |  |
| `permissions.contacts.edit` | boolean |  |
| `permissions.contacts.editSharedCustomViews` | boolean |  |
| `permissions.contacts.export` | boolean |  |
| `permissions.contacts.import` | boolean |  |
| `permissions.contacts.manageOwnCustomViews` | boolean |  |
| `permissions.contacts.reshareSharedCustomViews` | boolean |  |
| `permissions.contacts.shareOwnCustomViews` | boolean |  |
| `permissions.contacts.view` | boolean |  |
| `permissions.contracts.create` | boolean |  |
| `permissions.contracts.delete` | boolean |  |
| `permissions.contracts.deleteSharedCustomViews` | boolean |  |
| `permissions.contracts.edit` | boolean |  |
| `permissions.contracts.editSharedCustomViews` | boolean |  |
| `permissions.contracts.export` | boolean |  |
| `permissions.contracts.import` | boolean |  |
| `permissions.contracts.manageOwnCustomViews` | boolean |  |
| `permissions.contracts.reshareSharedCustomViews` | boolean |  |
| `permissions.contracts.shareOwnCustomViews` | boolean |  |
| `permissions.contracts.view` | boolean |  |
| `permissions.courses.create` | boolean |  |
| `permissions.courses.delete` | boolean |  |
| `permissions.courses.deleteSharedCustomViews` | boolean |  |
| `permissions.courses.edit` | boolean |  |
| `permissions.courses.editSharedCustomViews` | boolean |  |
| `permissions.courses.export` | boolean |  |
| `permissions.courses.manageOwnCustomViews` | boolean |  |
| `permissions.courses.reshareSharedCustomViews` | boolean |  |
| `permissions.courses.shareOwnCustomViews` | boolean |  |
| `permissions.courses.view` | boolean |  |
| `permissions.crmInteg.crmAccountsActivityCalls` | boolean |  |
| `permissions.crmInteg.crmAccountsActivityEvents` | boolean |  |
| `permissions.crmInteg.crmAccountsActivityTasks` | boolean |  |
| `permissions.crmInteg.crmAccountsInfo` | boolean |  |
| `permissions.crmInteg.crmAccountsNotes` | boolean |  |
| `permissions.crmInteg.crmAccountsPotentials` | boolean |  |
| `permissions.crmInteg.crmContactsActivityCalls` | boolean |  |
| `permissions.crmInteg.crmContactsActivityEvents` | boolean |  |
| `permissions.crmInteg.crmContactsActivityTasks` | boolean |  |
| `permissions.crmInteg.crmContactsInfo` | boolean |  |
| `permissions.crmInteg.crmContactsNotes` | boolean |  |
| `permissions.crmInteg.crmContactsPotentials` | boolean |  |
| `permissions.eventMapping.create` | boolean |  |
| `permissions.eventMapping.delete` | boolean |  |
| `permissions.eventMapping.deleteSharedCustomViews` | boolean |  |
| `permissions.eventMapping.edit` | boolean |  |
| `permissions.eventMapping.editSharedCustomViews` | boolean |  |
| `permissions.eventMapping.export` | boolean |  |
| `permissions.eventMapping.manageOwnCustomViews` | boolean |  |
| `permissions.eventMapping.reshareSharedCustomViews` | boolean |  |
| `permissions.eventMapping.shareOwnCustomViews` | boolean |  |
| `permissions.eventMapping.view` | boolean |  |
| `permissions.events.create` | boolean |  |
| `permissions.events.delete` | boolean |  |
| `permissions.events.deleteSharedCustomViews` | boolean |  |
| `permissions.events.edit` | boolean |  |
| `permissions.events.editSharedCustomViews` | boolean |  |
| `permissions.events.export` | boolean |  |
| `permissions.events.import` | boolean |  |
| `permissions.events.manageOwnCustomViews` | boolean |  |
| `permissions.events.reshareSharedCustomViews` | boolean |  |
| `permissions.events.shareOwnCustomViews` | boolean |  |
| `permissions.events.view` | boolean |  |
| `permissions.financeInteg.createContact` | boolean |  |
| `permissions.financeInteg.createEstimate` | boolean |  |
| `permissions.financeInteg.createInvoice` | boolean |  |
| `permissions.financeInteg.createSalesOrder` | boolean |  |
| `permissions.financeInteg.sendEstimate` | boolean |  |
| `permissions.financeInteg.sendInvoice` | boolean |  |
| `permissions.financeInteg.sendSalesOrder` | boolean |  |
| `permissions.financeInteg.viewEstimate` | boolean |  |
| `permissions.financeInteg.viewInvoice` | boolean |  |
| `permissions.financeInteg.viewSalesOrder` | boolean |  |
| `permissions.financeInteg.viewSubscription` | boolean |  |
| `permissions.gc.create` | boolean |  |
| `permissions.gc.delete` | boolean |  |
| `permissions.gc.edit` | boolean |  |
| `permissions.gc.view` | boolean |  |
| `permissions.im.create` | boolean |  |
| `permissions.im.delete` | boolean |  |
| `permissions.im.edit` | boolean |  |
| `permissions.im.view` | boolean |  |
| `permissions.imConversations.create` | boolean |  |
| `permissions.imConversations.delete` | boolean |  |
| `permissions.imConversations.deleteSharedCustomViews` | boolean |  |
| `permissions.imConversations.edit` | boolean |  |
| `permissions.imConversations.editSharedCustomViews` | boolean |  |
| `permissions.imConversations.export` | boolean |  |
| `permissions.imConversations.manageOwnCustomViews` | boolean |  |
| `permissions.imConversations.reshareSharedCustomViews` | boolean |  |
| `permissions.imConversations.shareOwnCustomViews` | boolean |  |
| `permissions.imConversations.view` | boolean |  |
| `permissions.imMessages.create` | boolean |  |
| `permissions.imMessages.delete` | boolean |  |
| `permissions.imMessages.deleteSharedCustomViews` | boolean |  |
| `permissions.imMessages.edit` | boolean |  |
| `permissions.imMessages.editSharedCustomViews` | boolean |  |
| `permissions.imMessages.export` | boolean |  |
| `permissions.imMessages.manageOwnCustomViews` | boolean |  |
| `permissions.imMessages.reshareSharedCustomViews` | boolean |  |
| `permissions.imMessages.shareOwnCustomViews` | boolean |  |
| `permissions.imMessages.view` | boolean |  |
| `permissions.kbCategory.admin` | boolean |  |
| `permissions.kbCategory.create` | boolean |  |
| `permissions.kbCategory.delete` | boolean |  |
| `permissions.kbCategory.edit` | boolean |  |
| `permissions.kbCategory.editAllArticles` | boolean |  |
| `permissions.kbCategory.export` | boolean |  |
| `permissions.kbCategory.import` | boolean |  |
| `permissions.kbCategory.manageKB` | boolean |  |
| `permissions.kbCategory.view` | boolean |  |
| `permissions.managerDashboard.allView` | boolean |  |
| `permissions.managerDashboard.customize` | boolean |  |
| `permissions.managerDashboard.myView` | boolean |  |
| `permissions.mobileapp.customMobileApps` | boolean |  |
| `permissions.mobileapp.deskapp` | boolean |  |
| `permissions.mobileapp.radar` | boolean |  |
| `permissions.modules.create` | boolean |  |
| `permissions.modules.delete` | boolean |  |
| `permissions.modules.deleteSharedCustomViews` | boolean |  |
| `permissions.modules.edit` | boolean |  |
| `permissions.modules.editSharedCustomViews` | boolean |  |
| `permissions.modules.export` | boolean |  |
| `permissions.modules.manageOwnCustomViews` | boolean |  |
| `permissions.modules.reshareSharedCustomViews` | boolean |  |
| `permissions.modules.shareOwnCustomViews` | boolean |  |
| `permissions.modules.view` | boolean |  |
| `permissions.products.create` | boolean |  |
| `permissions.products.delete` | boolean |  |
| `permissions.products.deleteSharedCustomViews` | boolean |  |
| `permissions.products.edit` | boolean |  |
| `permissions.products.editSharedCustomViews` | boolean |  |
| `permissions.products.export` | boolean |  |
| `permissions.products.import` | boolean |  |
| `permissions.products.manageOwnCustomViews` | boolean |  |
| `permissions.products.reshareSharedCustomViews` | boolean |  |
| `permissions.products.shareOwnCustomViews` | boolean |  |
| `permissions.products.view` | boolean |  |
| `permissions.radar.activities` | boolean |  |
| `permissions.radar.agentStats` | boolean |  |
| `permissions.radar.apiUsageAlerts` | boolean |  |
| `permissions.radar.auditLog` | boolean |  |
| `permissions.radar.averageHandlingTime` | boolean |  |
| `permissions.radar.channelTraffic` | boolean |  |
| `permissions.radar.contacts` | boolean |  |
| `permissions.radar.currentStats` | boolean |  |
| `permissions.radar.customerHappiness` | boolean |  |
| `permissions.radar.dailyToast` | boolean |  |
| `permissions.radar.dailyTrend` | boolean |  |
| `permissions.radar.dashboards` | boolean |  |
| `permissions.radar.exceptionHandling` | boolean |  |
| `permissions.radar.fcr` | boolean |  |
| `permissions.radar.feeds` | boolean |  |
| `permissions.radar.im` | boolean |  |
| `permissions.radar.kb` | boolean |  |
| `permissions.radar.liveTraffic` | boolean |  |
| `permissions.radar.manageRadar` | boolean |  |
| `permissions.radar.mostThreadedTickets` | boolean |  |
| `permissions.radar.quickView` | boolean |  |
| `permissions.radar.textContentProtection` | boolean |  |
| `permissions.radar.visualContentProtection` | boolean |  |
| `permissions.reports.create` | boolean |  |
| `permissions.reports.delete` | boolean |  |
| `permissions.reports.edit` | boolean |  |
| `permissions.reports.export` | boolean |  |
| `permissions.reports.view` | boolean |  |
| `permissions.setup.automation` | boolean |  |
| `permissions.setup.buttons` | boolean |  |
| `permissions.setup.chat` | boolean |  |
| `permissions.setup.community` | boolean |  |
| `permissions.setup.customerHappiness` | boolean |  |
| `permissions.setup.department` | boolean |  |
| `permissions.setup.email` | boolean |  |
| `permissions.setup.exportPortalUsers` | boolean |  |
| `permissions.setup.exportUsers` | boolean |  |
| `permissions.setup.featureConfig` | boolean |  |
| `permissions.setup.fetchAcrossDepartment` | boolean |  |
| `permissions.setup.gamification` | boolean |  |
| `permissions.setup.globalReports` | boolean |  |
| `permissions.setup.googleAnalytics` | boolean |  |
| `permissions.setup.im` | boolean |  |
| `permissions.setup.importHistory` | boolean |  |
| `permissions.setup.layouts` | boolean |  |
| `permissions.setup.localization` | boolean |  |
| `permissions.setup.manageAgents` | boolean |  |
| `permissions.setup.manageMarketplace` | boolean |  |
| `permissions.setup.managerDashboard` | boolean |  |
| `permissions.setup.massComment` | boolean |  |
| `permissions.setup.massReply` | boolean |  |
| `permissions.setup.moveRecords` | boolean |  |
| `permissions.setup.permission` | boolean |  |
| `permissions.setup.pinnedConversations` | boolean |  |
| `permissions.setup.portal` | boolean |  |
| `permissions.setup.portalUsers` | boolean |  |
| `permissions.setup.privacySettings` | boolean |  |
| `permissions.setup.rebranding` | boolean |  |
| `permissions.setup.recycleBin` | boolean |  |
| `permissions.setup.sandbox` | boolean |  |
| `permissions.setup.securitySettings` | boolean |  |
| `permissions.setup.shareSnippet` | boolean |  |
| `permissions.setup.signUpApproval` | boolean |  |
| `permissions.setup.social` | boolean |  |
| `permissions.setup.tabsAndFields` | boolean |  |
| `permissions.setup.teams` | boolean |  |
| `permissions.setup.telephony` | boolean |  |
| `permissions.setup.templates` | boolean |  |
| `permissions.setup.timeTracking` | boolean |  |
| `permissions.setup.webForm` | boolean |  |
| `permissions.setup.webhooks` | boolean |  |
| `permissions.social.twitterConversationReply` | boolean |  |
| `permissions.social.twitterPostCreate` | boolean |  |
| `permissions.social.twitterPostDelete` | boolean |  |
| `permissions.social.view` | boolean |  |
| `permissions.supportEmailAddress.create` | boolean |  |
| `permissions.supportEmailAddress.delete` | boolean |  |
| `permissions.supportEmailAddress.deleteSharedCustomViews` | boolean |  |
| `permissions.supportEmailAddress.edit` | boolean |  |
| `permissions.supportEmailAddress.editSharedCustomViews` | boolean |  |
| `permissions.supportEmailAddress.export` | boolean |  |
| `permissions.supportEmailAddress.manageOwnCustomViews` | boolean |  |
| `permissions.supportEmailAddress.reshareSharedCustomViews` | boolean |  |
| `permissions.supportEmailAddress.shareOwnCustomViews` | boolean |  |
| `permissions.supportEmailAddress.view` | boolean |  |
| `permissions.tasks.create` | boolean |  |
| `permissions.tasks.delete` | boolean |  |
| `permissions.tasks.deleteSharedCustomViews` | boolean |  |
| `permissions.tasks.edit` | boolean |  |
| `permissions.tasks.editSharedCustomViews` | boolean |  |
| `permissions.tasks.export` | boolean |  |
| `permissions.tasks.import` | boolean |  |
| `permissions.tasks.manageOwnCustomViews` | boolean |  |
| `permissions.tasks.reshareSharedCustomViews` | boolean |  |
| `permissions.tasks.shareOwnCustomViews` | boolean |  |
| `permissions.tasks.view` | boolean |  |
| `permissions.ticketLifeCycleData.create` | boolean |  |
| `permissions.ticketLifeCycleData.delete` | boolean |  |
| `permissions.ticketLifeCycleData.deleteSharedCustomViews` | boolean |  |
| `permissions.ticketLifeCycleData.edit` | boolean |  |
| `permissions.ticketLifeCycleData.editSharedCustomViews` | boolean |  |
| `permissions.ticketLifeCycleData.export` | boolean |  |
| `permissions.ticketLifeCycleData.manageOwnCustomViews` | boolean |  |
| `permissions.ticketLifeCycleData.reshareSharedCustomViews` | boolean |  |
| `permissions.ticketLifeCycleData.shareOwnCustomViews` | boolean |  |
| `permissions.ticketLifeCycleData.view` | boolean |  |
| `permissions.tickets.addFollowers` | boolean |  |
| `permissions.tickets.changeOwner` | boolean |  |
| `permissions.tickets.closeTicket` | boolean |  |
| `permissions.tickets.create` | boolean |  |
| `permissions.tickets.delete` | boolean |  |
| `permissions.tickets.deleteSharedCustomViews` | boolean |  |
| `permissions.tickets.deleteTags` | boolean |  |
| `permissions.tickets.edit` | boolean |  |
| `permissions.tickets.editSharedCustomViews` | boolean |  |
| `permissions.tickets.editTags` | boolean |  |
| `permissions.tickets.export` | boolean |  |
| `permissions.tickets.handleUnassigned` | boolean |  |
| `permissions.tickets.import` | boolean |  |
| `permissions.tickets.mailReview` | boolean |  |
| `permissions.tickets.mailSend` | boolean |  |
| `permissions.tickets.manageOwnCustomViews` | boolean |  |
| `permissions.tickets.mergeTickets` | boolean |  |
| `permissions.tickets.reshareSharedCustomViews` | boolean |  |
| `permissions.tickets.revokeBlueprint` | boolean |  |
| `permissions.tickets.shareOwnCustomViews` | boolean |  |
| `permissions.tickets.shareTickets` | boolean |  |
| `permissions.tickets.unassignedChangeOwner` | boolean |  |
| `permissions.tickets.view` | boolean |  |
| `permissions.timeEntry.create` | boolean |  |
| `permissions.timeEntry.delete` | boolean |  |
| `permissions.timeEntry.edit` | boolean |  |
| `permissions.timeEntry.view` | boolean |  |
| `permissions.zia.create` | boolean |  |
| `permissions.zia.delete` | boolean |  |
| `permissions.zia.edit` | boolean |  |
| `permissions.zia.view` | boolean |  |
| `type` | string |  |

## Native endpoint

Through the native Zoho Desk API, this operation is `GET myProfile` (base URL `https://desk.zoho.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-my-profile.md) for the provider-specific parameters and requirements.

