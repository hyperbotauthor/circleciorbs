# circleciorbs

## Enable CircleCI CLI GitHub

GitHub Organization page -> Settings / Third-party access -> enable

https://github.com/organizations/hyperchessbotauthor/settings/oauth_application_policy

## Create CircleCI API token

CircleCI User Settings ( at bottom ) -> Personal API Tokens -> Create New Token

store it in CIRCLECI_API_TOKEN env var locally

https://app.circleci.com/settings/user/tokens

## Install CircleCI CLI

```
curl -fLSs https://raw.githubusercontent.com/CircleCI-Public/circleci-cli/master/install.sh | bash
```

## Create CirleCI organization

```
circleci namespace create hyperchessbotauthor github hyperchessbotauthor
```

## Enable uncertified orbs

CircleCI Organization page ( can be selected from users ) -> Security -> check Allow Uncertified Orbs

https://app.circleci.com/settings/organization/github/hyperchessbotauthor/security

## CircleCI create orb

```
circleci orb create hyperchessbotauthor/builddockerimage
```

## CircleCI publish orb

```
circleci orb publish orb.yml hyperchessbotauthor/builddockerimage@1.0.0 --token $CIRCLECI_API_TOKEN
```
