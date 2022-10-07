# Ansible Playbook: mdatp_onboard_win
![GitHub last commit](https://img.shields.io/github/last-commit/lpwoodhouse/mdatp_onboard_win)
![GitHub repo file count](https://img.shields.io/github/directory-file-count/lpwoodhouse/mdatp_onboard_win)
![GitHub top language](https://img.shields.io/github/languages/top/lpwoodhouse/mdatp_onboard_win)

## Purpose

Onboards a Windows client to Microsoft Defender Advanced Threat Detection

## Requirements

community.windows

## Role Variables

```shell
# Important to provide a path to your onboarding package zip file which will be copied to the hosts during role execution.

zip_path: "files/WindowsDefenderATPOnboardingPackage.zip"

# Example of zip contents
#   - WindowsDefenderATPOnboardingScript
#   - <dir> OptionalParamsPolicy
#       - AtpConfiguration.admx
#       - <dir> en-US
#           - AtpConfiguration.adml
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

[![GitHub](https://img.shields.io/github/license/lpwoodhouse/mdatp_onboard_win)](LICENSE)

## Author Information

This playbook was created in 2022 by [Lee Woodhouse](https://www.leewoodhouse.com/)
