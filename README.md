# MacOS에서 iTems2를 이용해 북마크 관리하는 방법

## 1. 점프 호스트 설정 방법

https://github.com/20eung/ssh-proxyjump

## 2. Profile: JumpHost

- 위치: iTerms2 > Settings... (⌘ ,) > Profiles
- 새 프로파일 생성: ```Default```를 Duplicate Profile (⌘ =)
- General
  - Name: **JumpHost**
  - Tags: Proxy
  - Title: Name
  - Command: SSH ```jumphost```
    - [ ] Load shell integration automatically
      ![settings-profiles-general.png](/images/settings-profiles-general.png)
    - Configure...
      - [ ] SSH Integration
        ![settings-profiles-general-command-configure.png](/images/settings-profiles-general-command-configure.png)
     
## 3. Profile: target-server1

- 위치: iTerms2 > Settings... (⌘ ,) > Profiles
- 새 프로파일 생성: ```JumpHost```를 Duplicate Profile (⌘ =)
- General
  - Name: **target-server1**
  - Tags: Target-Server
  - Title: Name
  - Command: SSH ```target-server1```
    - [ ] Load shell integration automatically
    - Configure...
      - [ ] SSH Integration

## 4. Profile: target-server2

- 위치: iTerms2 > Settings... (⌘ ,) > Profiles
- 새 프로파일 생성: ```target-server1```를 Duplicate Profile (⌘ =)
- General
  - Name: **target-server2**
  - Tags: Target-Server
  - Title: Name
  - Command: SSH ```target-server2```
    - [ ] Load shell integration automatically
    - Configure...
      - [ ] SSH Integration

## 5. iTerms2 에서 사용 방법

- 위치: iTerms2 > Profiles > Open Profiles (⌘ O)
- Profiles 팝업창 왼쪽에는 Tags로 그룹핑, 오른쪽에 이름순으로 정렬되어 보임
![profiles.png](/images/profiles.png)
