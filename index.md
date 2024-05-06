# Lab Report 3

## Part 1
I will be looking at the bug in the `reversed(int arr[])` function

**1. A failure-inducing input for the buggy program**
```
  @Test
  public void testReversed1() {
    int[] input1 = {1, 2, 3, 4, 5};
    assertArrayEquals(new int[]{5, 4, 3, 2, 1}, ArrayExamples.reversed(input1));
  }
```

**2. An input that doesn't induce a failure**
```
  @Test
  public void testReversed2() {
    int[] input1 = { };
    assertArrayEquals(new int[]{ }, ArrayExamples.reversed(input1));
  }
```

**3. The symptom, as the output of running the two tests above**
![Image](output.PNG)

**4. The bug, as the before-and-after code change required to fix it**

Buggy Code
```
  static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = newArray[arr.length - i - 1];
    }
    return arr;
  }
```

Fixed Code
```
  static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      newArray[i] = arr[arr.length - i - 1];
    }
    return newArray;
}
```

**5. Brief Description**

   
**Code for `ChatServer.java`**


