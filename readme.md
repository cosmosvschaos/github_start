**[Step 1]**  `nums`에 대하여, 임의의 optimal swapping sequence(`OS`)를 생각하자.\
 `OS = [nums, nums1, nums2, …. , nums_final]`  where `nums_final` is a valid list\
**[Step 2]**  `nums` 원소 중 최솟값  `a_m`의 `nums` 내의 가장 왼쪽 인덱스를 `i`라고 하자.\
**[Step 3]** `OS` 의 원소 `nums_j` 내에서 `a_m`의 인덱스를 `m_j` 이라고 하자(1<=j<= final). 이 때 `m_j` != `m_(j-1)` 인 경우 해당 `num_j`를 `num_k`라고 하자. \
**[Step 4]** 이 경우, OS 내에서 그러한 `num_k`의 갯수 >= `i` 이다. (`a_m`  의 최초 위치가 `i` 였기 때문이다.)\
**[Step 5]**  `num_k_removed_OS` =  `OS` - {`num_j` | `m_j` != `m_(j-1)`  for (1<=j<= final) } 라고 하고, `num_k_removed_OS` 의 모든 원소에서 `a_m` 을 제거한다. 이 때 얻어지는 수열을 `smaller_OS` 라고 하자. \
**[Step 6]** len(`smaller_OS`) = len(`OS`) -  `num_k`의 갯수 >= len(`OS`) - i  from **step 4**\
**[Step 7]** len(`OS`) <= i + len(`smaller_OS`)가 된다. \
**[Step 8]** 이 때 `smaller_OS` 는 최초의 `nums`  에서 `a_m` 이 존재하지 않는다고 했을 때의 optimal swapping sequence일 수밖에 없다. (그렇지 않다면, OS 가 optimal swapping sequence 일수가 없기 때문이다.)
