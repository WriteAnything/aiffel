## 회고

일단 사진을 아웃포커싱하는 구현을 해보았다. segvalues, output = model.segmentAsPascalvoc(img_path)을 이용하여 사진 속의 각 대상을 세그먼테이션할 수 있었다. output의 색을 이용하여 각 대상을 필터할 수 있는 필터를 만들고 필터의 영역을 선명하게 그외 영역은 흐리게 만들어 대상을 아웃포커싱할 수 있었다.

개선할 수 있는 솔루션을 생각하지 못한 것은 아쉬운 점이다. 구현에 시간을 많이 사용하여 솔루션을 생각할 시간이 없었다. 이제 대상을 세그먼테이션하는 알고리즘을 학습할 것인데 궁금하다.

---

 🔑 **PRT(Peer Review Template)**

- 코더 : 이선열, 리뷰어 : 박장현  
<br/>
  
- [X]  **1. 주어진 문제를 해결하는 완성된 코드가 제출되었나요? (완성도)**
    - 문제에서 요구하는 최종 결과물이 첨부되었는지 확인
    - 문제를 해결하는 완성된 코드란 프로젝트 루브릭 3개 중 2개, 퀘스트 문제 요구조건 등을 지칭
      - 해당 조건을 만족하는 부분의 코드 및 결과물을 캡쳐하여 사진으로 첨부
  - 1.인물 모드 사진을 성공적으로 제작하였다. ![The portrait mode picture of a dog](https://github.com/JAMES-JHPARK/aiffel/blob/master/240605_Quest/screenshot/1.png)
  - 2.제작한 인물모드 사진들에서 나타나는 문제점을 정확히 지적하였다. ![The problem he identified](https://github.com/JAMES-JHPARK/aiffel/blob/master/240605_Quest/screenshot/2.png)
    - 갈색 강아지에 갈색 배경을 사용해서 색이 비슷하면 segmentation이 잘 안될 것이라는 가정사항을 확인하여 문제점을 지적하였습니다.
  - 3.인물모드 사진의 문제점을 개선할 수 있는 솔루션을 적절히 제시하였다.
    - 솔루션을 제시하지 못하였습니다.
    

~~- [ ]  **2. 프로젝트에서 핵심적인 부분에 대한 설명이 주석(닥스트링) 및 마크다운 형태로 잘 기록되어있나요? (설명)**~~ 
  ~~- [ ]  모델 선정 이유~~
  ~~- [ ]  Metrics 선정 이유~~  
  ~~- [ ]  Loss 선정 이유~~  

- [X]  **3. 체크리스트에 해당하는 항목들을 모두 수행하였나요? (문제 해결)**
    ~~- [ ]  데이터를 분할하여 프로젝트를 진행했나요? (train, validation, test 데이터로 구분)~~
    ~~- [ ]  하이퍼파라미터를 변경해가며 여러 시도를 했나요? (learning rate, dropout rate, unit, batch size, epoch 등)~~
    - [X]  각 실험을 시각화하여 비교하였나요?
      - 위 결과물 참고. 각 단계별 이미지 출력
      - ![Background compositing](https://github.com/JAMES-JHPARK/aiffel/blob/master/240605_Quest/screenshot/3.png)
    - [X]  모든 실험 결과가 기록되었나요?
      - 단계별 각종 좌표값 및 이미지 출력을 통한 결과 기록

- [X]  **4. 프로젝트에 대한 회고가 상세히 기록 되어 있나요? (회고, 정리)**
    - [X]  배운 점
      - Image segmentation과 인물모드 구현에 대해 배웠습니다.
    - [X]  아쉬운 점
      - 개선할 수 있는 솔루션을 생각하지 못한 것을 아쉬운 점으로 꼽았습니다.
    - [X]  느낀 점
      - Segmentation 기법과 알고리즘에 대해 학습할 것이라고 기대를 하고있습니다.
    - [X]  어려웠던 점
      - 구현에 많은 시간을 할애하여 시간이 부족했습니다.
