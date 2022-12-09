# microcontroller-the-running-line

```asm
org 0800
  mvi d, 0
  mvi A, 89
  out fb

  lxi h, 0900

  mov a, m
  out f8
  mvi a, 06
  out f9
  call 0860
  inx h

  mov a, m
  out f8
  mvi a, 39
  out f9
  call 0860
  inx h

  mov a, m
  out f8
  mvi a, 38
  out f9
  call 0860
  inx h

  mov a, m
  out f8
  mvi a, 77
  out f9
  call 0860
 inx h

  mov a, m
  out f8
  mvi a, 6d
  out f9
  call 0860
  inx h

  mov a, m
  out f8
  mvi a, 6d
  out f9
  call 0860
  inx h

  jmp 086a
  
  hlt

org 0860
  lxi b, 2fff
  dcx b
  mov a,b
  cmp d
  jnz 0862
  ret

org 086a
  mov a, l
  mvi e, 56
  cmp e
  jnz 0877
  lxi h, 0900
  jmp 0806
  
inr l
inr l
inr l
inr l
inr l
inr l
inr l
inr l
inr l
inr l

  jmp 0809
```

The task was to make a crawl line in the emulator. 

P.S. adding 10 did not work correctly, so I had to use 10 times increment

