# Code Peer Review

- 코더 :  김진홍 그루님
- 리뷰어 : 백기웅

---

## PRT(PeerReviewTemplate)

각 항목을 스스로 확인하고 체크하고 확인하여 작성한 코드에 적용하세요.

- [o] 코드가 정상적으로 동작하고 주어진 문제를 해결했나요?
- [o] 주석을 보고 작성자의 코드가 이해되었나요?
- [_] 코드가 에러를 유발할 가능성이 있나요?
- [o] 코드 작성자가 코드를 제대로 이해하고 작성했나요?
- [o] 코드가 간결한가요?

---

1. url을 통해 데이터셋 이미지를 불러와, 전처리를 세밀하게 잘 처리해 주셨습니다.

2.  Transfer Learning으로 Xception과 MobileNet을 사용하여 모델을 설계하였으며 classifier부분도 CNN과 pooling 등..<br>
   다양한 시도를 많이 하신 것 같았습니다.

   ```python
xception_base = Xception(include_top = False, weights = 'imagenet', input_shape = (height, width, 3))
xception_base.trainable = False

mobilenet_base = MobileNet(include_top = False, weights = 'imagenet', input_shape = (height, width, 3))
mobilenet_base.trainable = False
   ```
3. 두 모델 성능도 준수했으며 특히 Xception 모델의 성능은 상당히 우수했습니다.<br>
  (loss: 0.0227 - accuracy: 0.9963 - val_loss: 0.5634 - val_accuracy: 0.8544)

4. 생성된 모델을 이용하여 새로운 이미지에 적용해 보았다면 분명 좋은 결과를 보았을 것으로 생각됩니다.

---

### 리뷰어의 Comment
  
코드를 보며 많이 배웠습니다. 수고 하셨습니다~
