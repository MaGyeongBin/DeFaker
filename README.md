# DeFaker
### Members
##### 문경준 20207070 ansrudwns03290@gmail.com
##### 김승원 20207070 seungwon696@gmail.com
##### 송준홍 20207070 1dksektl1@gmail.com
##### 마경빈 2020707062 magyeongbin6@gmail.com

# 개요
### 장점:
1. 특징 추출 능력
- ResNet: 로컬 특징을 효과적으로 추출
- Vision Transformer: 전역 특징과 장거리 의존성 포착
- 두 아키텍처의 장점을 결합해 DeepFake의 미세한 조작 패턴 감지 가능
1. DeepFake 탐지에 적합한 이유
- 이미지의 다중 스케일 특징 포착 가능
- 얼굴의 부자연스러운 부분과 인공적 아티팩트 감지에 효과적
- 시간적 일관성 확인 가능 (비디오의 경우)
- 어텐션 메커니즘을 통한 조작 영역 집중 분석

### 구현 시 고려사항:
1. 데이터셋
- FF++ (FaceForensics++)
- DFDC (DeepFake Detection Challenge)
- Celeb-DF
- 다양한 DeepFake 생성 방식이 포함된 데이터셋 활용 권장
1. 모델 구조

```python
python
Copy
# 예시 구조
- ResNet 백본 (특징 추출)
- Convolutional Projection
- Vision Transformer 블록
- Classification Head
```
1. 학습 전략
- 두 단계 학습 (Two-stage training) 고려
- 데이터 증강 적극 활용
- 다양한 DeepFake 유형에 대한 견고성 확보