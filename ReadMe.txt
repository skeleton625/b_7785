백준 7785 문제 풀이중 입니다.

해당 문제는 잦은 시간 초과로인해 문제 해결에 어려움이 있었으므로 다음에 이와 같은 문제를 대비해야 합니다.

해당 문제는 사람들이 들어올 때 이름을 저장해 기억해 둔 다음 나갈때 이름을 제거해야하기 때문에 set container를

사용하는 것이 좋습니다.

( set 클래스의 경우 insert ( 추가 ) 함수와 erase ( 삭제 ) 함수로 저장된 데이터의 추가, 삭제를 간단하게 처리하기 때문 )

그리고 set container는 내부의 key값을 reverse 함수에 사용할 수 없으므로 vector 에 옮긴 다음 vector로 reverse 함수를 실행합니다.

해당 문제의 가장 큰 문제는 c++의 입출력 시간이 상당이 오래 걸린다는 것에 있습니다.

특히 endl의 경우 개행문자 뿐만 아니라 출력 버퍼를 비우는 역할까지 하기 때문에 출력 하나 하는동안 시간이 매우 오래걸립니다.

그렇기 c++을 통해 출력을 할 때는 endl을 사용하는 것 보다 개행문자'\n'만을 사용해서 출력을 하는 것이 좋습니다.

cin은 읽을 때 먼저 출력 버퍼를 비우기 때문에 이 또한 시간이 오래걸립니다.

cin.tie(NULL) 함수를 사용하면 cin과 cout의 묶음을 풀어주므로 입출력을 자주하는 경우에 사용하면 좋습니다.

그리고 ios_base::sync_with_stdio(false) 함수를 사용하면 C와 C++의 버퍼를 분리시켜 cin/cout이 더이상 stdin/stdout과 맞춰줄 필요가

없기 때문에 속도가 빨라집니다. 단 cin은 scanf, gets, getchar와 같이 사용하면 안되고 cout은 printf, puts, putchar와 같이 사용하면

안됩니다.
