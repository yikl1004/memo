### Git : Authentication failed 에러 처리

git 을 오랜만에 사용하는데 아래와 같은 오류 메시지가 발생했다.

> remote: HTTP Basic: Access denied
> fatal: Authentication failed for 'https://gitlab.com/myname/myproject'

전에 git 명령어로 설정한 데이터가 있는데 문제를 일으키는 상황같아 보였다. TortoiseGit 에서 Authentication data 를 Clear 해서는 초기화되지 않았다.

인증 관련 데이터를 초기화하기 위해서는 아래와 같이 처리하면 된다.

관리자 권한으로 명령창을 연다.
> 'git config --system --unset credential.helper' 를 실행한다.

만약 위 구문을 실행했음에도 해결이 되지 않을 시.
> global 영역 설정이 문제를 일으킬 수 있으니 'git config --global --unset credential.helper' 를 실행한다.
출처 : https://stackoverflow.com/questions/47860772/gitlab-remote-http-basic-access-denied-and-fatal-authentication
