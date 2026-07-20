# <img src="https://images.mindcloud.co/apps/icons/checkmob-software-logo_1781293656038.jpeg" alt="Checkmob logo" width="28" height="28"> Checkmob: Universal API

Checkmob verified draft: 63 actions are now in QA with live evidence across auth, client read/create/update flows, bulk client creation, client addresses, client notes, people create/get/update/delete flows, person-to-client linking, segment create/get/update/delete and link/unlink flows, checklist link/unlink flows, group update, service-order create/get/status-change/delete flows, and the supporting lookup/list families. The draft inventory totals 71 actions: 67 official Swagger-backed operations, one retained semantic duplicate search action, and three older candidate detail routes that are not present in Swagger and return HTTP 404. Eight actions remain blocked with explicit notes: Create Group (provider returns HTTP 500 even for Swagger-shaped payloads), Get/Update Person Address (tenant lacks a person record with an existing address row), Get/Update Service (tenant currently has zero service records), and the candidate Get Service Status by ID, Get Step by ID, and Get Temperature by ID routes that return HTTP 404.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/checkmob/latest
- **Category:** Support / Field Service
- **Vendor website:** https://www.checkmob.com
- **Vendor API docs:** https://api-integration.checkmob.com/index.html

