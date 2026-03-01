function* monthsGenerator() {
  const months = [
    "January",
    "February",
    "March",
    "April",
    "May",
    "June",
    "July",
    "August",
    "September",
    "October",
    "November",
    "December",
  ];

  let index = 0;

  while (true) {
    yield months[index];
    index = (index + 1) % months.length;
  }
}

const monthsIterator = monthsGenerator();
let count = 0;

const interval = setInterval(() => {
  const month = monthsIterator.next().value;
  const time = new Date().toLocaleTimeString();

  console.log(`${time} - ${month}`);

  count++;

  if (count === 12) {
    clearInterval(interval);
    console.log("Finished");
  }
}, 1000);
