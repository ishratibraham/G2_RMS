# G2_RMS
✅ if host_name is properly set in site_config.json

Make sure your site_config.json has:

"host_name": "https://your-site-url.com"


✅ Step 1: Enable OAuth 2 in ERPNext

Login to ERPNext as Administrator.

Go to:
Settings > OAuth Provider Settings
Enable OAuth Provider

✅ Step 2: Create OAuth Client (Application)
Navigate to:
Settings > OAuth Client
Click New to create a new OAuth Client.

Fill in the following:
App Name: G2_RMS

Redirect URIs: The URI where your .NET app will receive the authorization code (e.g., https://localhost:5001/signin-oidc for local development or your production URI).

Default Scope: all (or the scopes you need like all, openid, email).

Grant Type: Authorization Code (recommended for most secure apps).

Save it.

Note the generated:
Client ID
Client Secret



User = Offline POS User = user

after secussfull login need to create Offline User Login Details with field like user, log_in as Datetime, log_out as Datetime

and fetch data as

Company with default_currency = Offline POS User = company

POS Profile = disabled = 0,

warehouse = POS Profile = warehouse,

POS Payment Method = POS Profile = payments (table),

POS Payment Denomination = POS Profile = custom_denominations (table),

Customer Group = POS Profile = customer_groups (if exist in )

Customer = disabled = 0, is_frozen = 0

Item = disabled = 0

Item Price = selling = 1

Item Group = POS Profile = item_groups (POS Item Group) 

taxes from Item Group

Item Tax Template = disabled = 0

Sales Taxes and Charges Template = disabled = 0

Tax Rule



G2RMS Print Template = = POS Profile = 


Mode of Denomination = disabled = 0,


Delivery Charges = disabled = 0,

POS Offer = disabled = 0,

POS Coupon = disabled = 0, = company = company

Referral Code = disabled = 0, = company = company

