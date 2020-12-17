# Lombok����ע��

��ǰ��Java��Ŀ�г����̫�಻�ѺõĴ��룺POJO��Getter/Setter/toString�ȵȣ���Щ��������û��ʲô����������Ӱ���˴�������۵�ȱ�㣬��LombokӦ�˶�����

## ��װLombok

### ����Maven����
```xml
<dependency>
    <groupId>org.projectlombok</groupId>
    <artifactId>lombok</artifactId>
    <optional>true</optional>
</dependency>
```

### IDEA�а�װLombok���
���ε����FIle-Settings-Plugins���Ӳ����������Lombok���а�װ����װ֮��ѡLombok�������ɡ�
![img.png](../../images/java/lombok��װ.png)

## ע�����

### @Getter��@Setter
�������ϣ�Ϊ��������������Զ�����Getter������Setter����

```java
import lombok.Getter;
import lombok.Setter;

/**
 * @author: YS
 * @create: 2020-12-17
 **/
@Getter
@Setter
public class Student {
    int id;
    String name;
    int age;
}
```

### ToString
�Զ���дToString������������ƽʱʹ��IDEA�༭���Զ����ɵ�һ��

```java
/**
 * @author: YS
 * @create: 2020-12-17
 **/
@ToString
public class Student {
    int id;
    String name;
    int age;
}
```

### EqualsAndHashCode
�Զ�����equal(Object other)��hashCode()���������ĳЩ������������ע�⣬����ʹ��exclude�����ų�  
```java
import lombok.EqualsAndHashCode;

@EqualsAndHashCode
public class Student {
    int id;
    String name;
    int age;
}
```

```java
import lombok.EqualsAndHashCode;

//��name�����ų�����
@EqualsAndHashCode(exclude = "name")
public class Student {
    int id;
    String name;
    int age;
}
```
> �ʣ�Ϊʲô������equal(Object other)��hashCode()����Ū��һ��ע�⣬�����Ƿֿ�ʹ�ã�
> 
> ����java���й涨���������������ʱ�����ǵ�hashCode��һ����ȵģ����ǣ������������hashCode��ͬ������һ����ȣ���������Ϊ�˷�ֹΥ��java�涨���������

### @NoArgsConstructor
����һ���������κβ����Ĺ��캯��
```java
import lombok.NoArgsConstructor;

@NoArgsConstructor
public class Student {
    int id;
    String name;
    int age;
}
```

### @AllArgsConstructor
����һ���������в����Ĺ�����
```java
import lombok.AllArgsConstructor;

@AllArgsConstructor
public class Student {
    int id;
    String name;
    int age;
}
```

### @RequiredArgsConstructor
Ϊ���ض����������ɹ�����������ġ��ض�����������ָ��Щ����final���δʵ�����
```java
import lombok.RequiredArgsConstructor;

@RequiredArgsConstructor
public class Student {
    int id;
    final String name;
    int age;

    public static void main(String[] args) {
        Student student = new Student("33");
    }
}
```
��������ֻΪname����final���Σ����Է��֣�����ֻ������һ������name���ԵĹ����������⣬������е����Զ�û��final���εĻ���ʹ��@RequiredArgsConstructor������һ���޲εĹ�������  

### @Data
����һ�����ע�⣬�������ע�⣬�൱�ڼ�����@Getter��@Setter��@ToString��@EqualsAndHashCode��@RequiredArgsConstructor�����ע�⡣

### @Value
��Ҳ��һ�����ע�⣬���ǻ�����еı���������Ϊfinal�ģ������ľͺ�@Dataһ���ˡ���ͬ�ڼ�����@Getter��@ToString��@EqualsAndHashCode��@RequiredArgsConstructor���ĸ�ע�⣨��������������final�ģ�����û��@setterע���ˣ���

### @Builder
��ʽ��setֵд���������Ͼ��Ǹ����Ը�ֵ��������setter������Ҫ�еģ�һ����˵��@Builder���@Dataһ��ʹ�á�
```java
import lombok.Builder;
import lombok.Data;

@Builder
@Data
public class Student {
    int id;
    String name;
    int age;

    public static void main(String[] args) {
    Student student = 							Student.builder().id(1).name("water").age(18).build();
	}
}
```

### @Slf4j
�Զ����ɸ����log��̬�������Ϳ���ֱ�Ӵ�ӡ��־�ˣ�����ȥnewһ��log�ľ�̬�����ˡ�
```java
@Slf4j
public class Student {
    int id;
    String name;
    int age;

    public static void main(String[] args) {
        log.info("hello world");
    }
}
```










