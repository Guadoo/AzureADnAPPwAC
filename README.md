# Azure AD and App with policy and access control by users/groups

Reference video: 

<iframe src="//player.bilibili.com/player.html?aid=339457847&bvid=BV1QR4y157pM&cid=540198347&page=1" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true"> </iframe>

Reference doc: https://tech.aufomm.com/introduction-of-using-openid-connect-with-azure-ad/

## Azure AD - Create users and group

User1: AD_APP_Security01@rockjkmsn.onmicrosoft.com

User2: AD_APP_Security02@rockjkmsn.onmicrosoft.com

GROUP: AD_APP_Security_PoC

## App Registrations - Register App

Display Name                :   AD_APP_Security_PoC

Application(Client) ID      :   fbadf193-8446-42e7-96ff-xxxxxxxxx

Directory(tenant) ID        :   51f10121-ef02-43b6-807f-xxxxxxxxx

Selected                    :   Accounts in this organizational directory only (默认目录 only - Single tenant)

V2.0 Tokens                 :   Manifest > Modify "accessTokenAcceptedVersion": 2,"

Client Secret:
Certificates & secrets > Client secrets > Description:  AD_APP_Security_PoC_Secret
Expires    : 1 year 
Value      :  DNh8Q~HPnJJ9S6TWOKH9~mWoJz5p-IUAnfANVbZR

API permissions:
Microsoft APIs > Microsoft Graph (Commonly used Microsoft APIs) > Delegated permissions > Add permissions: email, openid

Token configuration:
Add optional claim > Token type = ID > Claim: email, family_name, given_name, ipaddr
