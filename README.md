
# Salesforce Mobile SDK - LWC Flow Example
![Status](https://img.shields.io/badge/status-Beta-yellowgreen)
![Geography](https://img.shields.io/badge/Geography-US-blue)

This repository contains a working build artifact of a Hybrid Remote mobile app built with the new Lightning Web Component embed technique to leverage LWC in the context of the Mobile SDK. In particular, this example has been built to show how a Lightning Flow can be embedded in a mobile app via the SDK.

This is super useful for customers who may be heavily using Flow and Lightning Web Components in the context of Community Cloud but who want to extend that investment to their wholly-owned native or hybrid Mobile apps by leveraging the Mobile SDK.

# Pre-reqs

* Xcode and Xcode CLI tools
* Node and npm
* Cocoa Pods

# Running The Baked App

1. Run the .workspace file in `mobileFlowEmbedTest/platforms/ios`
2. Change the build target in the selector to the right of the play / stop buttons on XCode to `yourAppName`
3. Build and see your magic app

# Instructions To Create Your Own App With This Repo

1. Fork the repo
2. Delete the `mobileFlowEmbedTest` folder
2. Run `npm install` from the root repo
2. Run `sfdx mobilesdk:hybrid:createwithtemplate -p ios -r HybridLwcTemplate -n yourAppName -k com.yourCompany.yourApp -o yourOrganization`
2. With SFDX, authorize your desired dev org.
3. Deploy the files in the `server` directory to your Salesforce org using `sfdx force:source:deploy -u <your dev org user name>  --sourcepath /HybridLwcTemplate/server/force-app/main/default/`
6. CD into the `/platform/ios` folder of your yourAppName directory
7. Run `pod install` 
8. Open the workspace file in yourAppName directory
9. Run the app

# Documentation

To learn more about the Salesforce Mobile SDKs, check out [our official documentation](https://developer.salesforce.com/docs/atlas.en-us.mobile_sdk.meta/mobile_sdk/intro.htm).

# Warranties

None. Use at your own risk. Purely demonstrative. Made with love.
