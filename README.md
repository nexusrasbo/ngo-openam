# [![N|Solid](https://ngazngoblobpub.blob.core.windows.net/static/nexus-go-logo-black.png)](https://www.nexusgroup.com/) meets FORGEROCK

## Setup IDP in FORGEROCK OpenAM
1. Login to OpenAM
2. Select Realm
3. Click "Configure SAMLv2 Provder"
4. Click "Created Hosted Identity Provider"
5. Setup IDP
    1. Give the IDP a name
    2. Assign a Signing key to the IDP
    3. Add IDP to a new circle of trust
    4. Add the following attribute mappings
        * cn -> cn
        * mail -> mail    
    5. Click Continue
    6. Click Finish
6. Download IDP metadata with URL https://<IdP_FQDN>/openam/saml2/jsp/exportmetadata.jsp?entityid=<name of IDP>

## Setup IDP in Nexus GO
1. Login to Nexus GO Portal
2. Click Services
3. Click "Signing"
4. Select your signing service
5. Click "Edit SAML IDP configuration"
6. Set a display name
7. Upload IDP metadata downloaded earlier
8. 
