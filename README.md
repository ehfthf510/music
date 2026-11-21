# 볼륨 플레이어 APK 만들기 (GitHub 자동 빌드)

PC에 아무것도 설치하지 않고, GitHub 웹사이트에서 APK를 만드는 방법입니다.

1. github.com에 로그인하고 오른쪽 위 + 버튼 → New repository 로 새 저장소를 만듭니다. 이름은 아무거나(예: volume-player), 공개/비공개 모두 가능합니다.
2. 저장소 화면에서 "uploading an existing file" 링크를 누르고, 이 압축을 푼 폴더 안의 모든 파일과 폴더(www, .github 포함)를 끌어다 놓은 뒤 Commit changes 를 누릅니다.
3. 위쪽 Actions 탭으로 가면 "Build APK" 작업이 자동으로 시작됩니다. 5~10분 걸립니다. (자동으로 시작되지 않으면 Build APK → Run workflow)
4. 초록색 체크가 뜨면 그 실행을 눌러 화면 맨 아래 Artifacts 의 volume-player-apk 를 내려받습니다. 압축을 풀면 app-debug.apk 가 있습니다.
5. APK를 폰으로 옮겨서 누르면 설치됩니다. "출처를 알 수 없는 앱" 허용을 물으면 허용해 주세요.

## 문제가 생기면
- Actions 탭에 "Build APK" 가 보이지 않으면 .github 폴더가 올라가지 않은 것입니다. 저장소에서 Add file → Create new file 을 누르고, 파일 이름 칸에 .github/workflows/build-apk.yml 을 입력한 뒤, 이 폴더의 build-apk.yml 내용을 붙여넣고 저장하세요.
- 빌드가 빨간색 X 로 끝나면 해당 실행 화면의 오류 내용을 그대로 복사해서 알려 주세요.

## 참고
- 폰 앱에서는 폴더 선택 버튼이 숨겨지고, 파일 선택(여러 곡 동시 선택)만 사용할 수 있습니다.
- 화면이 꺼지면 재생이 멈출 수 있습니다.
- 이 APK는 개인용 테스트 서명(debug)이라 구글 플레이 등록에는 쓸 수 없습니다.
