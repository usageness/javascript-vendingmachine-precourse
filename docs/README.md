<p align="middle" >
  <img width="200px;" src="https://github.com/woowacourse/javascript-vendingmachine-precourse/blob/main/images/beverage_icon.png?raw=true"/>
</p>
<h1 align="middle">자판기</h1>

## 요구사항
> 각 탭에 따라 적절한 기능을 수행할 수 있도록 구현한다.

### 상품 관리 탭
> 사용자는 자판기가 보유하고 있는 상품을 확인하고 추가할 수 있어야한다.

- [ ] 상품 관리 화면을 생성한다.
- [ ] 상품명, 가격, 수량을 입력해 상품을 추가할 수 있다.
- [ ] 상품 가격은 100원부터 시작하며 10원으로 나누어 떨어져야 한다.
- [ ] 사용자는 추가한 상품을 확인할 수 있다.

### 잔돈 충전 탭
> 사용자는 자판기의 보유 금액을 확인하고 추가할 수 있어야한다.

- [ ] 잔돈 충전 화면을 생성한다.
- [ ] 잔돈 충전 입력 요소에 금액을 입력 후, `충전하기` 버튼을 눌러 보유 금액을 충전할 수 있다.
- [ ] 자판기 보유 금액만큼의 동전이 무작위로 생성된다.
- [ ] 자판기가 이미 금액을 보유하고 있다면, 추가 금액 만큼의 동전을 생성하여 누적한다.

- 단, 동전 생성은 `MissionUtils` 라이브러리의 `Random.pickNumberInList`를 사용해 구한다.
```js
Random.pickNumberInList([1, 3, 10]); // 1
```

### 상품 구매 탭
> 사용자는 자판기에서 상품을 구매하고, 잔돈을 반환 받을 수 있다.

- [ ] 상품 구매 화면을 생성한다.
- [ ] 사용자는 투입할 금액을 입력한 후, `투입하기` 버튼을 눌러 금액을 투입할 수 있다.
- [ ] 사용자는 금액을 여러 번 누적해서 투입할 수 있다.
- [ ] 사용자는 `반환하기` 버튼을 눌러 잔돈을 반환 받을 수 있다.

**반환 시 유의사항**
- 잔돈은 자판기가 가진 동전 중 최소 개수의 동전으로 반환한다.
- 지폐를 잔돈으로 반환하는 경우는 없다.
- 잔돈을 반환할 수 없는 경우 반환할 수 있는 만큼만 반환한다.

### 공통
> 상단의 탭 메뉴가 존재하며, 각 탭에 따라 적절한 기능을 수행해야 한다.

- [x] 페이지 상단의 탭 메뉴를 생성한다.
- [x] 각 탭의 기능이 표시될 요소를 생성한다.
- [ ] `localStorage`를 이용하여, 새로고침하더라도 가장 최근에 작업한 정보들을 불러올 수 있도록 한다.