# circleciorbs

## Enable CircleCI CLI GitHub

GitHub Organization page -> Settings / Third-party access -> enable

## Create CircleCI API token

CircleCI User Settings ( at bottom ) -> Personal API Tokens -> Create New Token

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

## CircleCI create orb

```
circleci orb create hyperchessbotauthor/builddockerimage
```

## CircleCI publish orb

```
circleci orb publish orb.yml hyperchessbotauthor/builddockerimage@1.0.0 --token $CIRCLECI_API_TOKEN
```
