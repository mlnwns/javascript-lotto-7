# 🎰 로또

이 프로젝트는 사용자가 입력한 금액에 따라 로또 번호를 발행하고, 입력한 당첨 번호와 보너스 번호를 바탕으로 각 로또 번호의 당첨 여부를 확인합니다. 또한, 당첨된 등수와 수익률을 계산하여 사용자에게 제공합니다.

## 기능 목록

### 1. 로또 구입 금액 입력

- **구입 금액 입력받기**: 1,000원 단위로 로또 구입 금액을 입력 받습니다.
  - [x] 구입 금액이 숫자인지 확인.
    - [x] 숫자가 아닌 값을 입력한 경우 `[ERROR] 구입 금액은 숫자로만 이루어져야 합니다.` 출력.
  - [x] 구입 금액이 1,000원 단위인지 확인.
    - [x] 구입 금액이 1,000원으로 나누어떨어지지 않을 경우 `[ERROR] 구입 금액은 1,000원 단위여야 합니다.` 출력.
  - [x] 구입 금액이 1,000원 미만인지 확인.
    - [x] 구입 금액이 1,000원 미만인 경우 `[ERROR] 최소 구입 금액은 1,000원입니다.` 출력.

### 2. 로또 번호 발행

- **로또 번호 생성하기**: 1에서 45 사이의 중복되지 않는 6개의 숫자를 무작위로 뽑아 번호를 생성합니다.
  - [ ] 구입 금액을 1,000으로 나눈 수만큼 로또 번호를 생성.
  - [ ] Random 값 추출은 Random.pickUniqueNumbersInRange()를 활용.
  - [ ] 로또 번호가 오름차순으로 정렬되는지 확인.

### 3. 발행한 로또 수량과 번호 출력

- **로또 발행 결과 출력하기**: 발행한 로또의 수량과 각 로또 번호를 출력합니다.
  - [ ] 로또 구입 금액에 따른 로또 개수가 올바르게 출력되는지 확인.
  - [ ] 각 로또 번호가 오름차순으로 출력되는지 확인.

### 4. 당첨 번호 입력

- **당첨 번호 입력받기**: 쉼표(`,`)로 구분된 당첨 번호 6개를 입력받습니다.
  - [ ] 입력 형식이 올바른지 확인.
    - [ ] 쉼표로 구분되지 않은 형식이 입력된 경우 `[ERROR] 당첨 번호는 쉼표로 구분된 6개의 숫자여야 합니다.` 출력.
    - [ ] 숫자 이외의 값이 포함된 경우 `[ERROR] 당첨 번호는 숫자로만 이루어져야 합니다.` 출력.
  - [ ] 입력된 번호가 6개인지 확인.
    - [ ] 번호가 6개가 아닐 경우 `[ERROR] 당첨 번호는 6개여야 합니다.` 출력.
  - [ ] 번호가 중복되지 않았는지 확인.
    - [ ] 번호에 중복된 숫자가 있을 경우 `[ERROR] 당첨 번호는 중복될 수 없습니다.` 출력.
  - [ ] 각 번호가 1~45 범위 내의 숫자인지 확인.
    - [ ] 번호가 1~45 범위를 벗어날 경우 `[ERROR] 당첨 번호는 1에서 45 사이의 숫자여야 합니다.` 출력.

### 5. 보너스 번호 입력

- **보너스 번호 입력받기**: 보너스 번호 1개를 입력받아 유효성을 검사합니다.
  - [ ] 보너스 번호가 숫자인지 확인.
    - [ ] 숫자가 아닌 값을 입력한 경우 `[ERROR] 보너스 번호는 숫자여야 합니다.` 출력.
  - [ ] 입력된 번호가 1개인지 확인.
    - [ ] 번호가 1개가 아닐 경우 `[ERROR] 보너스 번호는 1개여야 합니다.` 출력.
  - [ ] 보너스 번호가 1~45 범위 내의 숫자인지 확인.
    - [ ] 보너스 번호가 1~45 범위를 벗어날 경우 `[ERROR] 보너스 번호는 1에서 45 사이의 숫자여야 합니다.` 출력.
  - [ ] 당첨 번호와 중복되지 않는지 확인.
    - [ ] 보너스 번호가 당첨 번호와 중복될 경우 `[ERROR] 보너스 번호는 당첨 번호와 중복될 수 없습니다.` 출력.

### 6. 당첨 내역 계산

- **당첨 결과 계산 및 출력하기**: 발행된 로또와 당첨 번호를 비교하여 당첨 결과를 출력합니다.
  - [ ] 3개 일치 시 5등(5,000원)당첨.
  - [ ] 4개 일치 시 4등(50,000원)당첨.
  - [ ] 5개 일치 시 3등(1,500,000원)당첨.
  - [ ] 5개 일치와 보너스 번호 일치 시 2등(30,000,000원)당첨.
  - [ ] 6개 일치 시 1등(2,000,000,000원)당첨.
  - [ ] 각 등수에 해당하는 로또 개수 출력.

### 7. 수익률 출력

- **수익률 계산 및 출력**: 수익률을 계산하여 소수점 둘째 자리까지 반올림하여 출력합니다.
  - [ ] 총 당첨 금액과 구입 금액을 비교해 수익률 계산.
  - [ ] 수익률을 소수점 둘째 자리에서 반올림하여 출력.
