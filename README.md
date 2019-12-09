# CPPD Application Environments

Contains manifest files that describe which things are deployed in each environment.

The manifest files are key/value pairs. Keys are the names of components/applications, and values are [SemVer](https://semver.org/) formatted version tags. Example:

```json
{
    "component_a": "<component a version tag>",
    "component_b": "<component b version tag>",
    ...
    "component_z": "<component z version tag>",
}
```

# Environments

## [**DEV**](DEV.json)

Used by the team to test new features in a prod-like environment, but doesn't hold real data. Updates to the environment can be request via pull request by any member of the team (although typically this will be an engineer in practice), but can only be approved by product managers.

__Note: Product manager enforcement of PR reviews will be enabled after the first successful releases to DEV have occurred.__

## [**PROD**](PROD.json)

Production environment capable of holding real data. Just used to research at the moment. Used by the team to test new features in a prod-like environment, but doesn't hold real data. Updates to the environment can be request via pull request by any member of the team (although typically this will be a product manager in practice), but can only be approved by service owners. 

__Note: Service Owners are not yet in GitHub, so we haven't implement this ownership mechanism yet.__

