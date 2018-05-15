module carry_skip_adder;
 input [3:0] a,b;
 parameter cin=1'b0;
 output [3:0] s;
 output reg cout;
 wire [3:0] c;
 wire [3:0] p;
 
 fa st1(s[0],c[0],a[0],b[0],cin);
 fa st2(s[1],c[1],a[1],b[1],c[0]);
 fa st3(s[2],c[2],a[2],b[2],c[1]);
 fa st4(s[3],c[3],a[3],b[3],c[2]);
 
 assign p[0]=a[0]^b[0];
 assign p[1]=a[1]^b[1];
 assign p[2]=a[2]^b[2];
 assign p[3]=a[3]^b[3];
  
 assign sel=p[0]&p[1]&p[2]&p[3];
 
 always@(*)
  case(sel)
   1:cout=cin;
   0:cout=c[3];
   
   endcase

endmodule
 
 module fa(s,co,a,b,c);
  input a,b,c;
  output s,co;
  assign s=a^b^c;
  assign co=(a&b)|(b&c)|(c&a);
  
  endmodule

