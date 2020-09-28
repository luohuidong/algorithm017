# Homework

## 26.删除排序数组中的重复项

```ts
function removeDuplicates(nums: number[]): number {
  let i = 0;

  for (let j = 1; j < nums.length; j++) {
    if (nums[i] !== nums[j]) {
      i++;
      nums[i] = nums[j];
    }
  }

  return i + 1;
}
```

## 283 移动零

```ts
function moveZeroes(nums: number[]): void {
  // 记录非零数字需要插入的数组索引位置
  let j = 0;

  for (let i = 0; i < nums.length; i++) {
    if (nums[i] !== 0) {
      // 将 i 索引位置的元素赋值到 j 索引位置上
      nums[j] = nums[i];

      // 如果 i !== j，表明此时 j 索引位置上的值是 0，需要将 i 索引位置的值替换为 0。
      if (i !== j) {
          nums[i] = 0;
      }

      j++;
    }
  }
};
```

## 66 加一

```ts
function plusOne(digits: number[]): number[] {
    const number = BigInt(digits.join("")) + BigInt(1);
  return [...String(number)].map((element) => Number(element));
};
```