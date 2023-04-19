# Lab-8_Group-5

### IT314-Software Engineering Lab-8
### Unit Testing with Jest in Javascript

#### Group - 5 Hostel Management System

# Group Details:

202001012	-	PRAKARSH MATHUR (Group Leader)

202001013	-	FAGUN VORA

202001018	- PATEL KAMAL HITESHBHAI

202001026	-	TEJANI ROMIT BHUPESHBHAI

202001032	-	HARSH CHIRAG PATEL

202001039	-	SHAH VISHRUT KUNAL

202001043	-	SHAH KIRTAN RAKESHKUMAR

202001054	-	BHAVSAR VUSHIL RAKESHKUMAR


### Testing authentication module in Javascript using Jest

There will be 4 type of testcases :

1. Empty input field


// test empty field error 
describe("POST /login", () => {
    test("it should return 452", async () => {
        const res = await request(baseURL).post("/login").send({
            email: "",
            password: ""
        });
        expect(res.statusCode).toEqual(452);

    });
});



2. Invalid Email id


// test invalid email error
describe("POST /login", () => {
    test("it should return 453", async () => {
        const res = await request(baseURL).post("/login").send({
            email: "20200018@daiict.ac.in",
            password: "kamaG5"
        });
        // console.log(res.statusCode);
        expect(res.statusCode).toEqual(453);

    });
});

3. Invalid Password



// test invalid password error
describe("POST /login", () => {
    test("it should return 454", async () => {
        const res = await request(baseURL).post("/login").send({
            email: "202001018@daiict.ac.in",
            password: "kamaG5"
        });
        // console.log(res.statusCode);
        expect(res.statusCode).toEqual(454);
    });
});


4. Correct credentials


// test valid login
describe("POST /login", () => {
    test("it should return 200", async () => {
        const res = await request(baseURL).post("/login").send({
            email: "202001018@daiict.ac.in",
            password: "kamalG5"
        });
        // console.log(res.statusCode);
        expect(res.statusCode).toEqual(200);
    });
});


![image](https://user-images.githubusercontent.com/96998317/233177716-6cca0c79-460f-4190-a56f-5172c70fa4b5.png)


![image](https://user-images.githubusercontent.com/96998317/233178171-281410b3-e36a-4878-b041-a4bc58fcbb20.png)

