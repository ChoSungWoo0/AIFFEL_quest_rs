# AIFFEL Campus Online Code Peer Review Templete
- 코더 : 조성우
- 리뷰어 : 이정우


# PRT(Peer Review Template)
- [ ]  **1. 주어진 문제를 해결하는 완성된 코드가 제출되었나요?**
    - 문제에서 요구하는 최종 결과물이 첨부되었는지 확인
        - 중요! 해당 조건을 만족하는 부분을 캡쳐해 근거로 첨부
     
          ![image](https://github.com/user-attachments/assets/ff7b3a9d-e729-4cf9-b899-442f153c00db)

        최종적으로 스티커가 적용되었습니다.
    
- [ ]  **2. 전체 코드에서 가장 핵심적이거나 가장 복잡하고 이해하기 어려운 부분에 작성된 
주석 또는 doc string을 보고 해당 코드가 잘 이해되었나요?**
    - 해당 코드 블럭을 왜 핵심적이라고 생각하는지 확인
    - 해당 코드 블럭에 doc string/annotation이 달려 있는지 확인
    - 해당 코드의 기능, 존재 이유, 작동 원리 등을 기술했는지 확인
    - 주석을 보고 코드 이해가 잘 되었는지 확인
        - 중요! 잘 작성되었다고 생각되는 부분을 캡쳐해 근거로 첨부
     
          def put_stickers(img, boxes, idx, sticker):
    img_height = img.shape[0]
    img_width = img.shape[1]

    x_min = int(boxes[idx][0] * img_width)
    y_min = int(boxes[idx][1] * img_height)
    x_max = int(boxes[idx][2] * img_width)
    y_max = int(boxes[idx][3] * img_height)
    
    w = x_max - x_min
    h = w//4
    
    sticker = cv2.resize(sticker, (w, h*2))
    
    sticker_area = img_raw[y_min-h:y_min+h, x_min:x_min+w] 
    
    img_raw[y_min-h:y_min+h, x_min:x_min+w] = np.where(sticker==0,sticker_area,sticker).astype(np.uint8)

저는 좀 헷갈렸던 부분인데 깔끔하게 하셔서 좋았습니다!
        
- [ ]  **3. 에러가 난 부분을 디버깅하여 문제를 해결한 기록을 남겼거나
새로운 시도 또는 추가 실험을 수행해봤나요?**
    - 문제 원인 및 해결 과정을 잘 기록하였는지 확인
    - 프로젝트 평가 기준에 더해 추가적으로 수행한 나만의 시도, 
    실험이 기록되어 있는지 확인
        - 중요! 잘 작성되었다고 생각되는 부분을 캡쳐해 근거로 첨부
     
![image](https://github.com/user-attachments/assets/3fc255ce-3cd7-4c9f-9aaf-a7cd1fa80ed6)


저는 epoch를 100으로 고정해서 따로 튜닝할 생각을 해보지 않아서 validation을 생각안했는데 잘참고가 되었습니다.


        
- [ ]  **4. 회고를 잘 작성했나요?**
    - 주어진 문제를 해결하는 완성된 코드 내지 프로젝트 결과물에 대해
    배운점과 아쉬운점, 느낀점 등이 기록되어 있는지 확인
    - 전체 코드 실행 플로우를 그래프로 그려서 이해를 돕고 있는지 확인
        - 중요! 잘 작성되었다고 생각되는 부분을 캡쳐해 근거로 첨부
     

![image](https://github.com/user-attachments/assets/10794e2e-e626-44bf-b220-e45acce56126)

네 잘 작성되었습니다.
        
- [ ]  **5. 코드가 간결하고 효율적인가요?**
    - 파이썬 스타일 가이드 (PEP8) 를 준수하였는지 확인
    - 코드 중복을 최소화하고 범용적으로 사용할 수 있도록 함수화/모듈화했는지 확인
        - 중요! 잘 작성되었다고 생각되는 부분을 캡쳐해 근거로 첨부

    
    ![image](https://github.com/user-attachments/assets/d894a6b8-8511-4975-b34f-869204527e7a)

네 잘 작성되었습니다.


# 회고(참고 링크 및 코드 개선)
```
# 리뷰어의 회고를 작성합니다.
# 코드 리뷰 시 참고한 링크가 있다면 링크와 간략한 설명을 첨부합니다.
# 코드 리뷰를 통해 개선한 코드가 있다면 코드와 간략한 설명을 첨부합니다.

저하고는 다른 시각으로 테스트 해보는 모습을 잘 참고할 수 있었습니다. 코드 짜는 부분에서도 참고 할 수 있어서 좋았습니다.


```
