### refusing to merge unrelated histories 오류

> 깃을 이용할 때 종종 **fatal: refusing to merge unrelated histories**라는 오류를 확인할 수 있습니다. 이 오류는 git push를 진행할 때나 혹은 git pull을 진행할 때 발견할 수 있는 오류입니다. 로컬 저장소와 원격지의 저장소의 기록(History)을 비교했을 때 소스코드의 차이가 심한 저장소의 경우, 병합 오류가 날 것을 대비하여 오류 메시지를 띄우는 것입니다.

이럴 때는 **--allow-unrelated-histories** 옵션을 붙여서 pull을 진행하시면 됩니다.  
merge, push를 진행 할때 위와 같은 에러가 나는 경우 동일한 옵션을 붙여 실행!

이렇게 merge를 하고 나면 conflict가 날텐데... 이 때는 직접 수동으로 수신반영 할지 여부를 결정하고 pull/push 를 하면 된다.

출처: https://ndb796.tistory.com/275