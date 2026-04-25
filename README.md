# Ochoice

<tr>
  <th>아키텍처</th>
  <td>
    [Client - Flutter App]<br>
    ├─ 일반 콘텐츠 요청<br>
    │&nbsp;&nbsp;↓<br>
    │&nbsp;&nbsp;[오초이스 Backend - SpringBoot]<br>
    │&nbsp;&nbsp;├─ PVS (회원/인증)<br>
    │&nbsp;&nbsp;├─ CMS (콘텐츠 메타데이터)<br>
    │&nbsp;&nbsp;├─ MBS (서비스/구매/권한)<br>
    │&nbsp;&nbsp;└─ MDS (관리/운영)<br>
    │&nbsp;&nbsp;↓<br>
    │&nbsp;&nbsp;[오초이스 Multi DRM License Server]<br>
    │&nbsp;&nbsp;↓<br>
    │&nbsp;&nbsp;[CDN / Streaming Server]<br>
    │&nbsp;&nbsp;↓<br>
    │&nbsp;&nbsp;[Flutter Player - BetterPlayer 기반 UI]<br>
    │<br>
    ├─ 딜라이브 대상 콘텐츠 요청<br>
    │&nbsp;&nbsp;↓<br>
    │&nbsp;&nbsp;[딜라이브 Backend Server]<br>
    │&nbsp;&nbsp;↓ 인증 / 콘텐츠 권한 / 재생 정보<br>
    │&nbsp;&nbsp;[딜라이브 NCG DRM License Server]<br>
    │&nbsp;&nbsp;↓<br>
    │&nbsp;&nbsp;[딜라이브 CDN / Streaming Server]<br>
    │&nbsp;&nbsp;↓<br>
    │&nbsp;&nbsp;[Flutter Player - Native Player 기반 UI]<br>
    │<br>
    └─ 공통 처리<br>
    &nbsp;&nbsp;&nbsp;├─ 콘텐츠 타입에 따라 오초이스 / 딜라이브 서버 분기<br>
    &nbsp;&nbsp;&nbsp;├─ DRM 방식별 재생 로직 분리<br>
    &nbsp;&nbsp;&nbsp;└─ Player UI 커스터마이징으로 동일한 사용자 경험 제공<br>
    <br>
    ↔ BigData / Ads / Admin System
  </td>
</tr>
