## Michaël Gugliandolo 40213419

## Step 1
a || (b && c)

## Step 2
### p = true
a = true <br/>
b = true <br/>
c = true <br/>

### p = false
a = false <br/>
b = false <br/>
c = false <br/>

@Test <br/>
public void step2TestTrue() { <br/>
  assertTrue(CheckIt.checkIt(true, true, true)); <br/>
}

@Test <br/>
public void step2TestFalse() { <br/>
  assertFalse(CheckIt.checkIt(false, false, false)); <br/>
}

## Step 3
We need two tests, one where both a and (b && c) are true, and another one where they're false.
- a, b, c = true
- a, b, c = false

@Test <br/>
public void step3TestTrue() { <br/>
  assertTrue(CheckIt.checkIt(true, true, true)); <br/>
}

@Test <br/>
public void step3TestFalse() { <br/>
  assertFalse(CheckIt.checkIt(false, false, false)); <br/>
}

## Step 4
Truth table:
![image](https://github.com/SOEN345-WINTER2024/logic-coverage-lab-Mika24boss/assets/77291451/b73eea08-5e84-4261-84bf-aaec802e2045)

We need 8 test cases:

@Test <br/>
public void step4Test1() { <br/>
  assertTrue(CheckIt.checkIt(true, true, true)); <br/>
} <br/>
@Test <br/>
public void step4Test2() { <br/>
  assertTrue(CheckIt.checkIt(true, true, false)); <br/>
} <br/>
@Test <br/>
public void step4Test3() { <br/>
  assertTrue(CheckIt.checkIt(true, false, true)); <br/>
} <br/>
@Test <br/>
public void step4Test4() { <br/>
  assertTrue(CheckIt.checkIt(true, false, false)); <br/>
} <br/>
@Test <br/>
public void step4Test5() { <br/>
  assertTrue(CheckIt.checkIt(false, true, true)); <br/>
} <br/>
@Test <br/>
public void step4Test6() { <br/>
  assertFalse(CheckIt.checkIt(false, true, false)); <br/>
} <br/>
@Test <br/>
public void step4Test7() { <br/>
  assertFalse(CheckIt.checkIt(false, false, true)); <br/>
} <br/>
@Test <br/>
public void step4Test8() { <br/>
  assertFalse(CheckIt.checkIt(false, false, false)); <br/>
} <br/>

## Step 5
### Pair 1
- a, b, c = true
- b = true and a, c = false
### Pair 2
- a, b = true and c = false
- c = true and a, b = false
### Pair 3
- a, c = true and b = false
- a, b, c = false

@Test <br/>
public void step5TestPair1() { <br/>
  assertTrue(CheckIt.checkIt(true, true, true)); <br/>
  assertFalse(CheckIt.checkIt(false, true, false)); <br/>
} <br/>
public void step5TestPair2() { <br/>
  assertTrue(CheckIt.checkIt(true, true, false)); <br/>
  assertFalse(CheckIt.checkIt(false, false, true)); <br/>
} <br/>
public void step5TestPair3() { <br/>
  assertTrue(CheckIt.checkIt(true, false, true)); <br/>
  assertFalse(CheckIt.checkIt(false, false, false)); <br/>
} <br/>

## Step 6
### Pair
- a, b, c = true
- b = true and a, c = false

@Test <br/>
public void step5TestPair1() { <br/>
  assertTrue(CheckIt.checkIt(true, true, true)); <br/>
  assertFalse(CheckIt.checkIt(false, true, false)); <br/>
} <br/>

## Step 7
¬a ^ b
