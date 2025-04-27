let users = {};
let currentUser;
l
//Create account functionality
document.getElementById('create-account-btn').addEventListener('click', () => {
    document.getElementById('login-form').style.display = none;
    document.getElementById('create-account-form').style.display = 'block';
})

document.getElementById('create-account-submit').addEventListener('click', (e) => {
    e.preventDefault();
    const newUsername = document.getElementById('new-username').value;
    const newPassword = document.getElementById('new-password').value;
    const idNumber = document.getElementById('ID-Number').value;
    const initialDeposit = parseFloat(document.getElementById('inital-deposit').value)

    if (!user[newUsername]) {
        users[newUsername] = {
            password: newPassword,
            balance: initialBalance,
            transactionHistory: []
        };

        console.log(`Account created for ${newUsername}`);
        document.getElementById('create-account-form').style.display = 'none';
    } else {
        console.log('Username already exists');
    }


    users[newUsername] = {
        password: newPassword,
        balance: initialDeposit,
        transactionHistory: []
    };

    document.getElementById('create-account-form').styledisplay = 'none';
    document.getElementById('login-form').style.display = 'block';
});

// Login functionality
document.getElementById('login-btn').addEventListener('click', (el) => {
    e.preventDefault();
    const username = document.getElementById('username').value;
    const password = document.getElementById('password').value;

    if (users[username] && users[username].password === password) {
        currentUser = username;
        document.getElementById('login-form').style.display = 'none';
        document.getElementById('account-overview').style.display = 'block';
        updateAccountOverview();
    } else {
        console.log('iNVALID CREDENTIALS');
    }
});

    // Assume login credentialsare valid for demonstration purposes
    document.getElementById('login-form').style.display = 'none';
    document.getElementById('account-overview').style.display = 'block';

//Deposit functionality
document.getElementById('deposit-btn').addEventListener('click', () => {
    const depositAmount = parseFloat(document.getElementById('deposit-amount').value);
    balance += depositAmount;
    transactionHistory.push(`Deposited $${depositAmount}`);
    document.getElementById('balance').textContent = balanc.toFixed(2);
    document.getElementById('transaction-history').innerHTML = '';
    transactionHistory.forEach((transaction) => {
        const li = document.createElement('li');
        li.textContent = transaction;
        document.getElementById(transaction-history).appendChildChild(li);
    });
    document.getElementById('deposit-form').style.display = 'none';
 });

    // Withdraw functionality
    document.getElementById('withdraw-btn').addEvent

