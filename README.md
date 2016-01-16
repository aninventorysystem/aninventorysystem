# Divens

An asset tracking system

## Schema

 - laptops
   - Assigned User ("unassigned" or <user>)
   - Serial Number
   - Asset Number
   - Company
   - Acquisition Date
   - Decommission Status
     - storage
     - sold
     - disposed
   - Notes
   - Model number (description is a part of model number)
 - power cables
   - asset number
   - assigned user
   - wattage
   - model
 - mifi devices
   - asset number
   - assigned user
   - model
   - ISP vendor
   - phone number
   - company
 - loaner
  - key of the asset that's checked out
  - loan duration
  - send notification?

## Assumptions

 - Assets are the central tenant of the system
 - Asset numbers are static, these do not change

## Requirements

 - Search ability, generic or filter based e.g. "serial number =" or "acquisition data = "?
 - Quick checkout process
 - Track assigned user history
 - API first class citizen
 - Export to CSV and PDF
 - Ability to see all assets assigned to a user
 - Mobile friendly

 - loaned equipment reminders directly to end-users? or perhaps just IT
 - All objects that are not assigned
 - Ability to create templates that define what attributes an object will have based on its type
 - Tie in to LDAP for user attributes
 - tie in with other systems, like helpdesk?

## Decisions

 - Name
 - Database back end - mysql
 - Api token auth
 - User prefs? Privs?

## API Design

 - get assets
   - individually (at least) or;
   - grouped (potentially)
 - create new assets
 - modify existing assets

/v1.0/assets/attributes/<attribute>/get
/v1.0/assets/attributes/<aattribute>/put
/v1.0/assets/attributes/<aattribute>/modify

## Roadmap

 - create static database schema for Laptops, Mifis, Power Cables

### 1.0

### 2.0

### 3.0

