set a 2

declare 
rn stud.rno%TYPE;
name stud.sname%TYPE;
cl stud.class%TYPE;
p stud.per %TYPE;
gr stud.grade%TYPE;
begin
rn:=&rn;
name:='&name';
cl:='&cl';
p:=&p;
IF(P>75)THEN
gr:='disitinction';
ELSIF((P>60)AND(P<75))THEN
gr:='first class';
ELSIF((P>50)AND(P<60))THEN
gr:='second class';
ELSIF((P>=35)AND(P<45))THEN
gr:='passed';
ELSE
gr:='failed';
END IF;
insert into stud values(rn,name,cl,p,gr);
dbms_output.put_line('insert record successfully');
end;
/

set a 1
declare
n number:=&n;
i number;
begin
FOR i IN 1..10 LOOP
dbms_output.put_line('n*i'||'='||n*i);
END LOOP;
END;
/

set a 3

declare
n number:=&n;
i number;
begin
IF(n>=0)THEN
dbms_output.put_line('no is positive'||i);
FOR i IN 1..n LOOP
IF(n mod 2<>0)THEN
dbms_output.put_line('no is odd'||i);
END IF;
END LOOP;
ELSE
dbms_output.put_line('no is negative' ||i);
END IF;
end;
/

set b

declare
i number;
begin
FOR i IN 1..10 LOOP
IF(i mod 2<>0)THEN
dbms_output.put_line('FYBBA(CA)');
ELSE
dbms_output.put_line('(ac)abbyf');
END IF;
END LOOP;
END;
/
