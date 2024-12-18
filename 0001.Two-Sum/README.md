常规的解法是使用两个循环，外层循环遍历数组中的每个元素，内层循环从当前元素的下一位开始遍历数组中剩余的元素。如果两个元素相等，则返回这两个元素的索引；如果不相等，继续下一次循环。
这种方式的时间复杂度为O(n^2)，其中n是数组的长度。

更高效的解法是使用哈希表。我们可以将数组中的元素作为键，索引作为值存储在哈希表中。这样，当我们遍历到某个元素时，就可以通过该元素求出与他相加等于target的值，并判断该值是否在哈希表中存在。存在则返回两个元素的索引，不存在则将该元素及其索引存入哈希表中。