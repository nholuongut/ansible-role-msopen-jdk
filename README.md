Ansible Role MSOpenJDK
=========

![](https://i.imgur.com/waxVImv.png)
### [View all Roadmaps](https://github.com/nholuongut/all-roadmaps) &nbsp;&middot;&nbsp; [Best Practices](https://github.com/nholuongut/all-roadmaps/blob/main/public/best-practices/) &nbsp;&middot;&nbsp; [Questions](https://www.linkedin.com/in/nholuong/)
<br/>

---

Install and configure [microsoft openjdk](https://docs.microsoft.com/de-de/java/openjdk/install) to host. This role will be download the openjdk archive, and place it to the local filesystem.

## Install

```
ansible-galaxy install nolte.msopenjdk
```

or add this to your ``requirements.yml``

```
- name: nolte.msopenjdk
```

and execute ``ansible-galaxy install -r requirements.yml``

## Usage

```
- hosts: all
  roles:
     - { role: nolte.msopenjdk }
```

By default we install a jdk 16, you can change this by edit the `jdk_used_version` variable possible Values are (`11` and `16`).

### Role Parameters 

| Value               | Default                                                                                       | Description                                                                   |
|---------------------|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| `jdk_used_version`  | `17`                                                                                          | Used JDk Version, supported Values are `11`,`16` and `17`.                         |
| `archiveFolderName` | `{{ jdk_versions[_jdk_used_version].archiveFolderName }}`                                     | Folder Name inside the Archive, used for build the Link to the java binaries. |
| `downloadUrl`       | `https://aka.ms/download-jdk/{{ jdk_versions[_jdk_used_version].archiveName }}`               | Download Url for the JDK Archive.                                             |
| `checksumUrl`       | `https://aka.ms/download-jdk/{{ jdk_versions[_jdk_used_version].archiveName }}.sha256sum.txt` | Text file with `sha256sum` informations.                                      |

## Development

For development and testing we use [molecule](https://molecule.readthedocs.io/en/latest/) in combination with docker.

```sh

# for install jdk 11 at molecule run
export MOLECULE_JDK_USED_VERSION="11"

molecule test

```

## Links

* Used at [nolte/ansible-minecraft](https://github.com/nholuongut/ansible-minecraft).

# 🚀 I'm are always open to your feedback.  Please contact as bellow information:
### [Contact ]
* [Name: nho Luong]
* [Skype](luongutnho_skype)
* [Github](https://github.com/nholuongut/)
* [Linkedin](https://www.linkedin.com/in/nholuong/)
* [Email Address](luongutnho@hotmail.com)

![](https://i.imgur.com/waxVImv.png)
![](Donate.png)
[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/nholuong)

# License
* Nho Luong (c). All Rights Reserved.🌟
