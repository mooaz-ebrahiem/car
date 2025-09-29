int motor1=4;
int motor2=7;
int motor3=8;
int motor4=12;
char c;

void setup() {
  // put your setup code here, to run once:
pinMode(motor1,OUTPUT);
pinMode(motor2,OUTPUT);
pinMode(motor3,OUTPUT);
pinMode(motor3,OUTPUT);
Serial.begin(9600);

}

void loop() {
  // put your main code here, to run repeatedly:

if(Serial.available()){

  c=Serial.read();
}
    if(c=='B'){
    digitalWrite(motor1,1);
    digitalWrite(motor3,1);
    digitalWrite(motor2,0);
    digitalWrite(motor4,0);
    }
    else if(c=='F'){
    digitalWrite(motor1,0);
    digitalWrite(motor3,0);
    digitalWrite(motor2,1);
    digitalWrite(motor4,1);
    }
    else if(c=='R'){
    digitalWrite(motor1,0);
    digitalWrite(motor3,1);
    digitalWrite(motor2,1);
    digitalWrite(motor4,0);
    }
    else if(c=='L'){
    digitalWrite(motor1,1);
    digitalWrite(motor3,0);
    digitalWrite(motor2,0);
    digitalWrite(motor4,1);
    }
    else if(c=='S'){
    digitalWrite(motor1,0);
    digitalWrite(motor3,0);
    digitalWrite(motor2,0);
    digitalWrite(motor4,0);
    }
}
