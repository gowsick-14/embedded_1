# embedded_1
my led blibking in esp32 using register level program 
accessing register instead of using inbuild libraries
the code is :
void setup()
{
  (*(volatile uint32_t *) 0x3FF44020) |= (1 << 4);
}
void loop()
{
  (*(volatile uint32_t *) 0x3FF44004) |=(1 << 4);  
  delay(2000);  
  (*(volatile uint32_t *) 0x3FF44004) &= ~(1 << 4); 
  delay(2000);  
}
also i upload this videos in youtbe the link is :
https://youtu.be/aPz9wEdrup0?si=yNFZqzv6SW5eW7O-
