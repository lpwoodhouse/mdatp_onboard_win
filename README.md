# Onboard Microsoft Defender Advanced Threat Protection (MDATP) (Windows Hosts)
![Windows](https://img.shields.io/badge/Microsoft%20Windows-232F3E?style=flat&logo=windows&logoColor=3a77b3)
[![playbook](https://img.shields.io/badge/Ansible-Playbook-blue)](site.yml)
![GitHub last commit](https://img.shields.io/github/last-commit/lpwoodhouse/mdatp_onboard_win)
![GitHub repo file count](https://img.shields.io/github/directory-file-count/lpwoodhouse/mdatp_onboard_win)
![GitHub top language](https://img.shields.io/github/languages/top/lpwoodhouse/mdatp_onboard_win)
[![GitHub](https://img.shields.io/github/license/lpwoodhouse/mdatp_onboard_win)](LICENSE)
## Purpose

Onboards a Windows client to Microsoft Defender Advanced Threat Detection.

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

## Author Information

This playbook was created in 2022 by [Lee Woodhouse](https://www.leewoodhouse.com/)
