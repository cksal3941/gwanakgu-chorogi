# 관악구 초록이

<img src="chorogi/public/images/sprout.png" width="160" alt="초록이 캐릭터" />

버리기 애매한 형광등, 의류, 폐건전지 등을 근처 어디에 버릴 수 있는지 지도로 알려주는 서비스입니다.
길에서 마주치는 초록색 새싹 캐릭터 **초록이**와 함께, 분리배출을 조금 더 쉽고 친숙하게 만들고 싶어서 만들었습니다.

- 배포 링크: https://chorogi.vercel.app
- GitHub: https://github.com/cksal3941/gwanakgu-chorogi
- Figma: https://www.figma.com/design/dpS1oKrRGHwYgzsEbdztUe/%EA%B4%80%EC%95%85%EA%B5%AC-%EC%B4%88%EB%A1%9D%EC%9D%B4?node-id=0-1&t=FOgoIU1LvnPTVHKi-1

## 프로젝트 소개

- 기간: 2023.08, 1주일
- 인원: 3명 (기획/디자인/개발 전 과정을 함께 진행)
- 서울시·관악구 공공데이터의 수거함 주소 정보를 카카오맵 좌표로 변환해 데이터로 구성하고, 카카오맵 API로 지도 위에 표시했습니다.
- 짧은 기간 안에 완성하는 것을 목표로 데이터는 하드코딩으로 구성했습니다.

## 주요 기능

지도에서 안내하는 4가지 배출/재활용 정보를 제공합니다.

| 카테고리 | 설명 |
| --- | --- |
| 의류 수거함 | 옷, 신발 등을 재활용/재사용할 수 있는 수거함 위치 안내 |
| 폐건전지·형광등 수거함 | 중금속이 포함된 폐건전지·형광등의 올바른 배출 장소 안내 |
| 네프론(수퍼빈) | 투명 페트병·캔을 넣으면 포인트로 보상받을 수 있는 순환 자원 회수 로봇 위치 안내 |
| 기부하기 | 사용하지 않는 물품을 기부할 수 있는 굿윌스토어 위치 안내 |

각 카테고리는 지도에서 위치를 확인하는 화면과, 왜 분리배출이 필요한지 · 무엇을 넣어도 되고 안 되는지를 설명하는 상세 페이지로 구성되어 있습니다.

## 캐릭터, 초록이

메인 캐릭터인 초록이는 [Nomad Sculpt](https://nomadsculpt.com/)로 직접 조각한 3D 캐릭터입니다. 점토를 빚듯 브러시로 얼굴과 몸을 만들고 색칠·재질 작업까지 iPad에서 진행한 뒤, 서비스 전반의 로딩 화면과 헤더 등에서 사용했습니다.

## 기술 스택

- **React 18** (Create React App)
- **react-router-dom** — 페이지 라우팅
- **react-kakao-maps-sdk** — 카카오맵 연동
- **react-slick / slick-carousel** — 홈 화면 캐러셀
- **@iconify/react** — 아이콘
- **react-device-detect** — 모바일/브라우저 환경 분기
- **Vercel** — 배포

## 사용한 오픈소스

- [Create React App](https://github.com/facebook/create-react-app)
- [react-router-dom](https://github.com/remix-run/react-router)
- [react-kakao-maps-sdk](https://github.com/JaeSeoKim/react-kakao-maps-sdk)
- [react-slick](https://github.com/akiran/react-slick) / [slick-carousel](https://github.com/kenwheeler/slick)
- [Iconify](https://iconify.design/)
- [react-device-detect](https://github.com/duskload/react-device-detect)
- [카카오맵 API](https://apis.map.kakao.com/)
- [서울 열린데이터광장 / 공공데이터포털](https://data.seoul.go.kr) — 수거함 주소 데이터

## 실행 방법

```bash
cd chorogi
npm install
npm start
```

카카오맵을 띄우려면 `chorogi/public/index.html`의 스크립트 태그에 본인의 카카오 JavaScript 키를 넣고, [카카오 디벨로퍼스](https://developers.kakao.com)에서 사용할 도메인(`http://localhost:3000` 등)을 Web 플랫폼에 등록해야 합니다.

## 팀원

- [@cksal3941](https://github.com/cksal3941)
- [@hanna0115](https://github.com/hanna0115)
- [@Ji2unKo](https://github.com/Ji2unKo)
