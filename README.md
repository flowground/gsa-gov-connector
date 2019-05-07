# ![LOGO](logo.png) Discovery Market Research **flow**ground Connector

## Description

A generated **flow**ground connector for the Discovery Market Research API (version 0.1).

Generated from: https://api.apis.guru/v2/specs/gsa.gov/0.1/swagger.json<br/>
Generated at: 2019-05-07T17:42:13+03:00

## API Description

<p>This API drives the <a href="https://discovery.gsa.gov">Discovery Market Research Tool</a>.
It contains information on the vendors that are part of the OASIS and OASIS Small Business contracting vehicles, such as their contracting history, their elligibility for contract awards, and their small business designations.
To learn more about the tool, please visit <a href="https://discovery.gsa.gov">Discovery</a> or see the README on our <a href="https://github.com/PSHCDevOps/discovery">GitHub repository</a>.</p>
<p><strong>Please note that the base path for this API is <code>https://api.data.gov/gsa/discovery/</code></strong></p>
<p>It requires an API key, obtainable at <a href="http://api.data.gov/">api.data.gov</a>.
It must be passed in the <code>api_key</code> parameter with each request.</p>

## Authorization

This API does not require authorization.

## Actions

### This endpoint returns contract history from FPDS for a specific vendor

> <p>This endpoint returns contract history from FPDS for a specific vendor. The vendor's DUNS number is a required parameter. You can also filter contracts by their NAICS code to find contracts relevant to a particular category.</p>

*Tags:* `contracts`

#### Input Parameters
* `duns` - _required_ - A 9-digit DUNS number that uniquely identifies a vendor (required).
* `naics` - _optional_ - a six digit NAICS code used to filter by contracts with a certain NAICS
* `sort` - _optional_ - a field to sort on. Choices are date, status, agency, and amount
* `direction` - _optional_ - The sort direction of the results. Choices are asc or desc.
* `page` - _optional_ - the page to start on. Results are paginated in increments of 100. Begins at page=1.

### This endpoint returns metadata for the most recent data loads of SAM and FPDS data

> <p>This endpoint returns metadata for the most recent data loads of SAM and FPDS data. It takes no parameters.</p>

*Tags:* `metadata`

### This endpoint lists all of the NAICS codes that are relevant to the OASIS family of vehicles

> <p>This endpoint lists all of the NAICS codes that are relevant to the OASIS family of vehicles. It takes no parameters.</p>

*Tags:* `naics`

### This endpoint returns a single vendor by their 9 digit DUNS number

> <p>This endpoint returns a single vendor by their 9 digit DUNS number. DUNS numbers can be looked up in the <a href="https://www.sam.gov">System for Award Management</a> by vendor name.</p>

*Tags:* `vendor`

#### Input Parameters
* `duns` - _required_ - a nine digit DUNS number that uniquely identifies the vendor (required)

### This endpoint returns a list of vendors filtered by a NAICS code

> <p>This endpoint returns a list of vendors filtered by a NAICS code. The NAICS code maps to an OASIS pool and is used to retrieve vendors in that pool only.</p><br/>
> <p>OASIS pools are groupings of NAICS codes that have the same small business size standard. Because contracts solicited to OASIS vendors can only be issued to one pool, much of the data is presented as part of a pool grouping. Using the NAICS code is a shortcut, so that you don't have to explicitly map the NAICS code to a pool in OASIS yourself.</p><br/>
> <p>Vendors can also be filtered by a particular setaside. Valid values for the setasides are two-character codes which include:</p><br/>
> <ul><br/>
> <li>A6 (8(a))</li><br/>
> <li>XX (Hubzone)</li><br/>
> <li>QF (service disabled veteran owned)</li><br/>
> <li>A2 (women owned)</li><br/>
> <li>A5 (veteran owned)</li><br/>
> <li>27 (small disadvantaged business).</li><br/>
> </ul>

*Tags:* `vendors`

#### Input Parameters
* `naics` - _required_ - a six digit NAICS code (required)
* `setasides` - _optional_ - a comma delimited list of two character setaside codes to filter by.  Ex. setasides=A6,A5  will filter by 8a and veteran owned business.
* `vehicle` - _optional_ - Choices are either oasis or oasissb. Will filter vendors by their presence in either the OASIS unrestricted vehicle or the OASIS Small Business vehicle.

## License

**flow**ground :- Telekom iPaaS / gsa-gov-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
