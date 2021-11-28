# Cycle GAN: 박태성(UC 머클리)

### Prisma: 사진을 그림처럼 바꿔주는 AI
### -> 그림을 사진으로 바꾸는 인공지능

## pix2pix: 사진을 사진으로 바꾸는 작업
- Self-Supervised
- 흑백사진을 컬러로 바꾸는 경우 결과를 모르니 중간값을 선택하는 경향이 있음
- -> 사람이 할 수 있다면 딥러닝 네트워크도 할 수 있지 않나해서 출현한 것이 **GAN**
- "위조지폐 만들기" + "위조지폐 감별하기"
<img src="https://user-images.githubusercontent.com/68985625/143727933-efc94c01-c28f-4235-8871-cdbf279884d9.png">

## CycleGAN
- 대칭적인 로스를 기반으로 동시에 훈련시켜 4가지 로스를 합친 결과가 CycleGAN이다.
<img src="https://user-images.githubusercontent.com/68985625/143728114-d250bf43-91e7-4360-a5d7-45e87f3e9652.png">
- encoding <-> decoding의 방식에서 벗어나 U-Net을 사용
- **U-Net**: 스킵 커넥션 이용, 바틀넥에 들어갔다 나올 때 많이 없어짐
- **ResNet**: 뎁스도 있고 바틀넥은 없어 디테일을 간직할 수 있었음. 그러나 메모리를 많이 사용함