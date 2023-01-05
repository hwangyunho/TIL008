# TIL008

## CRUD

* 데이터 값 변경(설정)
>* UPDATE MY_EMP
>* SET DEPTNO = ( 	SELECT DEPTNO
>    * FROM MY_EMP
>    * WHERE EMPNO = 7934)
>* WHERE EMPNO = 7698;
* 데이터 값 추가
> * INSERT INTO MY_EMP(EMPNO, ENAME) VALUES(0002,'홍길동2');
* 데이터 값 삭제
> * DELETE FROM MY_EMP
WHERE JOB = (SELECT M_NEW.JOB FROM( SELECT JOB FROM MY_EMP WHERE ENAME ='WARD')
			M_NEW);
* 트랜잭션
> * SET AUTOCOMMIT = FALSE;
> * START TRANSACTION;
>
> * '''DELETE FROM MY_EMP
WHERE DEPTNO = 10;'''
> * COMMIT;
> * '''~~~~~'''
> * ROLLBACK;

***

## 프로시저
* CALL MY_프로시저(a,b,c);
> * my_db에 있는 MY_프로시저에 a,b,c를 넣고 부른다.
* 프로시저 만들기
>CREATE PROCEDURE `MY_프로시저` (a int, b int, (out) c varchar(10) ) --변수 앞에 out을 넣어 리턴값을 만들수도 있다
>* BEGIN
>* 변수에 맞게 작동 시킬 sql문
>* END
