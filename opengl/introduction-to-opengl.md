# Introduction to OpenGL

OpenGL은 application이 장치의 그래픽스 서브시스템에 접근하고 제어하기 위해 사용하는 인터페이스다. 서브시스템에 대한 인터페이스를 표준화하면 이식성을 증대시킬 수 있고, 소프트웨어 개발자들은 기반 플랫폼의 세부사항을 고민하는 대신 흥미로운 컨텐츠를 제작하거나 application의 성능을 향상시킬 수 있는데, 바로 OpenGL은 하위 그래픽스 서브시스템을 제어하기 위한 API인 것이다.

## OpenGL graphics pipeline

![Simplified graphics pipeline is not found]

둥근 박스는 `고정 함수` 스테이지이며, 일반 박스는 `프로그래밍 가능` 스테이지다.  
프로그래밍 가능 스테이지에서는 개발자가 제공한 쉐이더를 수행한다.  

## OpenGL core profile

1992년 1월 첫 OpenGL 1.0이 발표된 이래로 현재는 4.3에 이르기까지 10여회가 넘는 release가 있었다. 그 때마다 하위 호환성을 중요하게 생각해왔고 현재도 그러하다. 하지만 이러한 하위 버전 호환성은 비용이 크다. 게다가 현대 그래픽스 프로세스 아키텍처에는 맞지 않는 경우도 있다. 새로운 기능과 예전 기능과 어떻게 상호 작용하는지 정하는 것이 쉽지 않을 뿐 아니라 많은 경우, 새로운 기능을 OpenGL에 깔끔하게 제공하는 것이 거의 불가능한 경우도 있다.  
이러한 이유로 2008년에 OpenGL ARB는 OpenGL을 두 가지 profile로 분리하게 되었다. 하나는 `Core profile`인데 현대 그래픽스 하드웨어로 가속하지 못하는 많은 기존 기능을 제거했다. `Compatibility profile`은 OpenGL 1.0까지의 모든 버전과 하위 호환성을 유지한다. compatibility profile이 존재하는 이유는 기존 application을 유지 보수할 때를 위한 것이므로 새로운 application을 개발할 때는 core profile 사용이 강력히 권고된다.

[Simplified graphics pipeline is not found]:https://people.eecs.ku.edu/~jrmiller/Courses/672/InClass/MaterialsFromElsewhere/SimplifiedGraphicsPipeline_FromSuperBible.png
