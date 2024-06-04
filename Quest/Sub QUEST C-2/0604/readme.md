🔑 **PRT(Peer Review Template)**
Reviewer : 맹주현

- [ ]  **1. 주어진 문제를 해결하는 완성된 코드가 제출되었나요? (완성도)**
    - 문제에서 요구하는 최종 결과물이 첨부되었는지 확인
    - 문제를 해결하는 완성된 코드란 프로젝트 루브릭 3개 중 2개, 
    퀘스트 문제 요구조건 등을 지칭
        - 해당 조건을 만족하는 부분의 코드 및 결과물을 캡쳐하여 사진으로 첨부
        - 
![화면 캡처 2024-06-04 173147](https://github.com/WriteAnything/aiffel/assets/168398983/2d9292a4-3c8b-4602-9cf2-f681a837b40d)

얼굴 영역과 랜드마크를 정확하게 검출하고, 스티커 사진을 합성시키는 데 성공하였다. (O)

![화면 캡처 2024-06-04 173354](https://github.com/WriteAnything/aiffel/assets/168398983/c224521a-3af6-4bf0-8b8b-02c559d88f0d)

refined_x = x - 130
refined_y = y - 130
landmark 값이 아닌, 절대적 수치로 연산을 하셔서 약간 어긋나지 않았나 싶습니다. landmark index를 활용하거나 수치값을 개선해봐도 좋을 것 같아요!

img_sticker = 255 - img_sticker

img_bgr[refined_y:refined_y +img_sticker.shape[0], refined_x:refined_x+img_sticker.shape[1]] = \
    np.where(img_sticker==0,sticker_area,img_sticker).astype(np.uint8)
plt.imshow(cv2.cvtColor(img_bgr, cv2.COLOR_BGR2RGB)) # rgb만 적용해놓은 원본 이미지에 왕관 이미지를 덮어 씌운 이미지가 나오게 된다.
plt.show()

흰색 배경이 나오는 error를 255 - sticker로 해결 하셨는데, 이 부분 때문에 수염이 흰색으로 바뀌어서 적용된 것 같습니다. 
저는 img_sticker는 그대로 두고 np.where 부분의 sticker_area 와 img_sticker 의 위치를 변경해서 해결했습니다!

여러 각도에서 실험하신 내용은 피어리뷰 시간에 잘 설명해주셨는데 나중에 추가적으로 결과물들 업로드해서 수정하시면 퍼실님들이 보고 평가해주실 것 같아요.


- [ ]  **2. 프로젝트에서 핵심적인 부분에 대한 설명이 주석(닥스트링) 및 마크다운 형태로 잘 기록되어있나요? (설명)**
     주석이 빽빽히 작성되어 있었는데, 노드에 적혀있던 주석에 추가적으로 업데이트 된 내용이 부족했습니다!
노드 내용 중 개념 설명이나, 새로운 라이브러리를 소개하는 부분을 추가적으로 작성하고, 적용된 코드를 간단하게 설명만 해줘도 훨씬 깔끔해질 것 같습니다! 

- [ ]  **3. 체크리스트에 해당하는 항목들을 모두 수행하였나요? (문제 해결)**
    - [ ]  데이터를 분할하여 프로젝트를 진행했나요? (train, validation, test 데이터로 구분)
    - [ ]  하이퍼파라미터를 변경해가며 여러 시도를 했나요? (learning rate, dropout rate, unit, batch size, epoch 등)
    - [ ]  각 실험을 시각화하여 비교하였나요?
    - [ ]  모든 실험 결과가 기록되었나요?
     
오늘의 주제는 모델 학습이 아니라 배포된 라이브러리 모델 실습이었기 때문에 이 부분은 넘어가겠습니다. 

- [ ]  **4. 프로젝트에 대한 회고가 상세히 기록 되어 있나요? (회고, 정리)**
    - [X]  배운 점
    - [ ]  아쉬운 점
    - [X]  느낀 점
    - [ ]  어려웠던 점
     
  
     ![화면 캡처 2024-06-04 175559](https://github.com/WriteAnything/aiffel/assets/168398983/0313fac3-11ec-4a37-9b81-637b729143de)

  
