# Ansible Role: mdatp_onboard_win

Onboards a Windows client to Microsoft Defender Advanced Threat Detection

## Requirements

community.windows

## Role Variables

```shell
# Important to provide a path to your onboarding package zip file which will be copied to the hosts during role execution.

zip_path: "files/WindowsDefenderATPOnboardingPackage.zip"

# Example of package contents
    - WindowsDefenderATPOnboardingScript
    - OptionalParamsPolicy
        - AtpConfiguration.admx
        - en-US
            - AtpConfiguration.adml
```
## Dependencies

None

## Example Playbook
```yaml
    - hosts: all
      vars:
        - zip_path: "files/WindowsDefenderATPOnboardingPackage.zip"
      roles:
        - mdatp_onboard_win
```

## License

GNU General Public Licence v3.0

## Author Information

This role was created in 2022 by [Lee Woodhouse](https://www.leewoodhouse.com/)
