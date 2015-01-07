# CircleCI-iOS-TestFlight-Sample
Demonstrate how to deploy an iOS app automatically to testflight using CircleCI.

## How to set up your project
1. Copy the circle.yml into your repo (replace app name, developer name and provisionin profile uuid)
2. Create the folder "scripts/"
3. Export the following things from the Keychain app
  1. "Apple Worldwide Developer Relations Certification Authority" into scripts/apple.cer
  2. Your iPhone Distribution certificate into scripts/dist.cer
  3. Your iPhone Distribution private key into scripts/dist.p12 (choose a password)
4. Copy your provisioning profiles into scripts/profile/
5. Add the following settings in "Environment Variable" menu on CircleCI
  1. KEY_PASSWORD=YOUR_KEY_PASSWORD
  2. TEAM_TOKEN=TESTFLIGHT_TEAM_TOKEN
  3. API_TOKEN=TESTFLIGHT_API_TOKEN
6. Copy add-key.sh, remove-key.sh and testflight.sh into scripts/