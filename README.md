Used PostgreSQL 
CREATE TABLE users (
    id UUID DEFAULT gen_random_uuid() PRIMARY KEY,
    name TEXT NOT NULL,
    sex TEXT CHECK (sex IN ('Male', 'Female', 'Other')),
    age INT CHECK (age >= 18),
    created_at TIMESTAMP DEFAULT now()
);


INSERT INTO users (name, sex, age) VALUES
('Ana Anusca', 'Female', 25),
('Bobescu Bob', 'Male', 30),
('Vasile Andrei', 'Other', 22);

To connect your HTML form to PostgreSQL I need a backend server (the credentials for this will be taken from a .env file)
Also, I will need to create  a js file, to send form data to my backend. 
For deploiement, I can use Vercel. 


