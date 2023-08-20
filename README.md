# 1.Class

**클래스(Class)**: 클래스는 객체를 정의하기 위한 템플릿 또는 청사진입니다. 클래스는 데이터 멤버와 멤버 함수로 구성되며, 객체의 속성과 동작을 정의합니다. 즉, 클래스는 객체가 가져야 할 데이터와 그 데이터를 조작하는 메서드들을 모아놓은 개념적인 구조입니다. 클래스는 타입을 정의하는 것으로, 객체를 생성하기 위한 기본 틀을 제공합니다.

**객체(Object)**: 객체는 클래스의 인스턴스(instance)로, 클래스로부터 생성된 실제 데이터가 담긴 것입니다. 객체는 클래스의 멤버 변수에 저장된 데이터와 클래스에 정의된 메서드에 의해 처리되는 동작을 가지며, 프로그램에서 실제로 사용되는 주체입니다. 객체는 실제로 메모리에 할당되어 사용되는 인스턴스로, 클래스의 특성을 따르면서도 고유한 상태를 가집니다.

간단히 말하면, 클래스는 추상화된 개념으로 객체를 정의하기 위한 설계도이고, 객체는 실제로 메모리에 할당되어 데이터와 동작을 가지는 실체입니다. 클래스는 객체의 특성과 동작을 정의하는 것이며, 객체는 클래스의 정의를 바탕으로 생성되어 사용됩니다.

**멤버 변수(Member Variables)**: 멤버 변수는 클래스 내부에서 선언되는 변수로, 객체의 상태를 나타내는 데이터를 저장하는 데 사용됩니다. 클래스의 각 객체는 각자의 멤버 변수를 가지며, 이 변수들은 객체마다 다른 값을 가질 수 있습니다. 예를 들어, 자동차 클래스의 멤버 변수로 '속도', '색상', '연식' 등이 있을 수 있습니다.

**멤버 함수(Member Functions)**: 멤버 함수는 클래스 내부에서 정의되는 함수로, 객체의 동작을 정의하고 구현하는 데 사용됩니다. 멤버 함수는 클래스의 멤버 변수에 접근하여 데이터를 처리하거나 변경할 수 있습니다. 예를 들어, 자동차 클래스의 멤버 함수로 '가속', '브레이크', '라디오 켜기' 등의 동작을 구현할 수 있습니다.

이렇게 멤버 변수와 멤버 함수는 클래스가 가지는 데이터와 동작을 정의하는 중요한 요소입니다. 클래스의 멤버 변수와 멤버 함수는 객체 지향 프로그래밍에서 객체의 특성과 동작을 모델링하는 데 사용되며, 클래스와 객체의 주요 특징 중 하나입니다.

```cpp
#include <iostream>

class Car {
private:
    // 멤버 변수 (클래스 내부의 데이터)
    int speed;
    std::string color;

public:
    // 생성자 (객체를 초기화하는 함수)
    Car(int initialSpeed, const std::string& initialColor) {
        speed = initialSpeed;
        color = initialColor;
    }

    // 멤버 함수 (클래스 내부의 동작)
    void Accelerate(int amount) {
        speed += amount;
        std::cout << "Accelerating by " << amount << " km/h.\n";
    }

    void Brake(int amount) {
        speed -= amount;
        std::cout << "Braking by " << amount << " km/h.\n";
    }

    void DisplayInfo() {
        std::cout << "Car color: " << color << ", Speed: " << speed << " km/h\n";
    }
};

int main() {
    // Car 클래스의 객체 생성 및 초기화
    Car myCar(0, "Blue");

    // 객체의 동작 실행
    myCar.Accelerate(50);
    myCar.Brake(20);

    // 객체 정보 출력
    myCar.DisplayInfo();

    return 0;
}

```

위 코드에서 주석이 달린 각 문장은 다음과 같은 역할을 수행합니다:

* `class Car { ... }`: Car 클래스 정의 시작.
* `private:`: 이후에 선언되는 멤버 변수는 클래스 내부에서만 접근 가능.
* `int speed;`, `std::string color;`: 멤버 변수로 speed와 color를 선언.
* `public:`: 이후에 선언되는 멤버 함수는 외부에서도 접근 가능.
* `Car(int initialSpeed, const std::string& initialColor) { ... }`: 생성자 정의. 객체를 초기화할 때 호출됨.
* `void Accelerate(int amount) { ... }`: 객체의 동작을 정의하는 Accelerate 멤버 함수.
* `void Brake(int amount) { ... }`: Brake 멤버 함수. 객체의 동작을 정의.
* `void DisplayInfo() { ... }`: 객체의 정보를 출력하는 DisplayInfo 멤버 함수.
* `Car myCar(0, "Blue");`: Car 클래스의 객체 myCar 생성 및 초기화.
* `myCar.Accelerate(50);`, `myCar.Brake(20);`: 객체의 동작 실행.
* `myCar.DisplayInfo();`: 객체 정보 출력.

