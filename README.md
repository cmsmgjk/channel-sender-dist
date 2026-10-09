# 채널 발송기 — 배포

설치 파일과 설정만 두는 곳입니다. 소스는 들어 있지 않습니다.

| 파일 | 쓰임 |
|---|---|
| `config.json` | 설치된 확장이 켜질 때 읽습니다. 선택자·공지·최신 버전 정보 |
| Releases | 설치용 zip |

## 설치

[Releases](../../releases) 에서 최신 zip 을 받아 압축을 풀고,
`chrome://extensions` → 개발자 모드 → **압축해제된 확장 프로그램을 로드** → 푼 폴더 선택.

자세한 내용은 zip 안의 `다른PC에설치하기.txt` 에 있습니다.

## config.json

```json
{
  "inputSelector": "#chatWrite",
  "sendSelector":  "#kakaoWrap button.btn_submit",
  "notice":        "",
  "latestVersion": "0.3.0",
  "downloadUrl":   "...zip",
  "changes":       ["바뀐 내용"]
}
```

- `inputSelector` · `sendSelector` — 카카오가 채팅 화면을 바꾸면 **이 두 줄만 고치면**
  설치된 모든 PC 가 다음 실행에서 복구됩니다. 재설치가 필요 없습니다.
- `notice` — 채우면 확장 화면 위에 노란 띠로 공지가 뜹니다. 비우면 안 보입니다.
- `latestVersion` — 설치된 버전보다 높으면 업데이트 버튼에 빨간 점이 붙습니다.

학생 명단·대화방 연결은 각 PC 크롬 안에만 저장되며 이곳과 무관합니다.
