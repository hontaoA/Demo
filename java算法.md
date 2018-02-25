# java算法

- demo1

```java
public class Example01 {
  
	public static void main(String[] args) {
		int[] num = {2,7,11,15};
		for(int i:twoSum_2(num,22)){
			System.out.print(i+"\t");
		}
	}
	
	public static int[] twoSum(int[] nums,int taraget){
		int[] index = new int[2];
		for (int i = 0; i < nums.length; i++) {
			for (int j = i+1; j < nums.length; j++) {
				if ((nums[i]+nums[j])==taraget) {
					index[0]=i;
					index[1]=j;
				}
			}
		}
		return index;
	}
	
	public static int[] twoSum_2(int[] nums,int taraget){
		int[] result = new int[2];
		Map<Integer,Integer> map = new HashMap<Integer,Integer>();
		for(int i = 0 ;i < nums.length;map.put(nums[i], i++)){
			if (map.containsKey(taraget-nums[i])) {
				return new int[]{map.get(taraget-nums[i]),i};
			}
		}
		return new int[]{0,0};
	}
	
	
}	
```

