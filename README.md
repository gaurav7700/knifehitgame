# knifehitgame

var array1 = [
  {
    bank: "abank",
    formID: "oiytghgvyguygvhbhugyv",
  },
  {
    bank: "bank",
    formID: "oiytghgvygufcgvhbygvhbhugyv",
  },
  {
    bank: "abank",
    formID: "oi56ytghgvyguygvhbhugyv",
  },
  {
    bank: "bank",
    formID: "oiytghgvyguygvhbh678iugyv",
  },
  {
    bank: "abank",
    formID: "oiytghgv567uhyguygvhbhugyv",
  },
];


const sumWithInitial = array1.reduce((accumulator, currentValue) => {
  if (accumulator[currentValue.bank]) {
    accumulator[currentValue.bank] = {
      bank: currentValue.bank,
      formid: [...accumulator[currentValue.bank].formid, currentValue.formID],
    };
  } else {
    accumulator[currentValue.bank] = {
      bank: currentValue.bank,
      formid: [currentValue.formID],
    };
  }
  return [accumulator]
}, {})
