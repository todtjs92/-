# 음원특성만을 고려한 음악추천프로그램
## 시연화면
![시연화면](https://user-images.githubusercontent.com/59354220/94268613-67272b00-ff78-11ea-8b9b-8c8d754c6f05.png)


음원특성만을 고려하여 추천해준다면 추천리스트에 자주오르는 곡들이 아니라
처음 들어보지만 내가 찾던 노래와 정말 유사한 곡을 찾을 수 있지 않을까?
라는 생각에 시도해봤던 프로젝트.

처음하는 프로젝트라 실력이 많이부족했지만 파이썬 실력을 기르는데 많이 도움이 되었다.

## 방법
1. 10000개 정도의 곡을 유튜브에서 크롤링하여 모음 
2. 이 곡들에서 centroid, flatness, tonetzz 를 구하여 3개의 축으로 설정하고 csv파일로 저장.
3. 사용자가 음악을 입력하면 그 음악과 거리가 가장가까운 곡들 5개를 추천해주고 그에대한 평가를 하게함
4. 평가를 바탕으로 가중치를 바꾸어 추가적으로 추천.

## 시연영상
https://www.youtube.com/watch?v=0BxyGrvqsK0

### 프로젝트를 하며 아쉬웠던 점. 
https://medium.com/p/59f2ad967b31/edit

### spectral centroid와 flatness 에 대하여
https://bit.ly/308WyJl
### .
https://bit.ly/30a67aO