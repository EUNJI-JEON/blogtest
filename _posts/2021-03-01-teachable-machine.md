---

title: "[Teachable Machine] 코딩없이 머신러닝 모델 만들기"
---

Teachable Machine
Train a computer to recognize your own images, sounds, & poses.
A fast, easy way to create machine learning models for your sites, apps, and more – no expertise or coding required.

 

구글에서 제공하는 Teachable machine을 활용하면 코딩없이 머신러닝 모델을 만들 수 있다. 연예인 사진 데이터를 크롤링해 학습 데이터로 활용하면 동물상테스트나 관상테스트 같은 사이트에 사용된 머신러닝 모델을 만들 수 있는 것이다.

Teachable machine을 활용해 머신러닝 모델을 만드는 방법은 간단하다.

 

1. New Project 를 생성한다. 이 때 가장 먼저 Image project인지 Audio project 인지  Pose Project 인지 선택한다.  

2. Image Project를 선택한 경우 웹캠을 활용하거나 업로드 방식을 통해 직접 모은 사진 데이터를 업로드해 학습 데이터로 활용할 수 있다.

3. 클래스별로 나눈 이미지 데이터를 업로드한 다음 Train model을 눌러 트레이닝한다.

4. Preview를 통해 원하는 모델이 만들어졌는지 확인한다. 이 때 사람 얼굴을 학습한 사진이면 전신보다는 얼굴에만 포커스된 사진들만 모아 학습 데이터로 활용해야 정확도가 높아진다. preview로 확인한 아웃풋이 만족스럽지 않은 경우 학습 데이터를 다시 모으거나 클리닝해 재학습하는 것이 필요한다. 학습 데이터의 조건이 동일할수록 이를테면 사람 얼굴을 학습하는 경우 얼굴이 확대된 흑백 사진으로 통일한다거나 해야 정확도가 높아진다. 

5. Export Model을 누르면 만든 머신러닝 모델을 다운로드 할 수 있는 압축파일이 제공된다. 혹은 직접 다운로드하지 않고 웹이나 앱에 붙일 수 있도록 javascript 링크를 복사해도 된다. 

 

teachablemachine의 활용 방안은 무궁무진하다. 예를 들어 식물이나 동물 사진을 학습한 모델을 만들어 식물 맞추기, 동물 맞추기 같은 교육 웹이나 앱을 만들 수도 있을 것이다. 모델을 만드는데 어떤 코딩도 필요하지 않으니 기존에 머신러닝 모델을 직접 만드는데 필요했던 수고를 덜어주는 것만은 분명한 것 같다. teachablemachine는 더 빠르고 다양하게 프로토타입을 제작해본다거나 빨리 출시해 테스트해보는 린한 프로젝트들에 확실히 유용할 것으로 보인다.
