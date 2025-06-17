document.addEventListener("DOMContentLoaded", function() {
  const companyGradeSelect = document.getElementById('companyGrade');
  const categoryTypeSelect = document.getElementById('categoryType');
  const numSubcategoriesInput = document.getElementById('numSubcategories');
  const registrationDurationSelect = document.getElementById('registrationDuration');
  const reyadaCardCheckbox = document.getElementById('reyadaCardHolder');
  
  const reviewFeeElement = document.getElementById('reviewFee');
  const registrationFeeElement = document.getElementById('registrationFee');
  const subcategoryFeeElement = document.getElementById('subcategoryFee');
  const totalFeeElement = document.getElementById('totalFee');

  // Fee rules
  const feeRules = {
    review: {
      excellent: 10,
      first: 10,
      second: 5,
      third: 5,
      fourth: 5
    },
    registration: {
      excellent: 200,
      first: 200,
      second: 150,
      third: 100,
      fourth: 50
    },
    subcategory: 5
  };

  // Function to remove "Consultancy" option if Grade 4 is selected
  function adjustConsultancyOption() {
    const selectedGrade = companyGradeSelect.value;
    const consultancyOption = categoryTypeSelect.querySelector('option[value="consultancy"]');
    
    if (selectedGrade === 'fourth') {
      consultancyOption.disabled = true;
      consultancyOption.selected = false;
    } else {
      consultancyOption.disabled = false;
    }
  }

  // Event listener for form changes
  function calculateFees() {
    const selectedGrade = companyGradeSelect.value;
    const selectedCategories = Array.from(categoryTypeSelect.selectedOptions).map(option => option.value);
    const numSubcategories = parseInt(numSubcategoriesInput.value) || 0;
    const registrationDuration = reyadaCardCheckbox.checked ? 2 : parseInt(registrationDurationSelect.value);
    const reyadaDiscount = reyadaCardCheckbox.checked;

    // Calculate review fee
    const reviewFee = feeRules.review[selectedGrade];

    // Calculate registration fee
    const registrationFee = feeRules.registration[selectedGrade] * selectedCategories.length * registrationDuration;

    // Calculate subcategory fee
    const subcategoryFee = feeRules.subcategory * numSubcategories;

    // Apply Reyada discount
    const registrationFeeAfterDiscount = reyadaDiscount ? Math.max(0, registrationFee - (feeRules.registration[selectedGrade] * selectedCategories.length * 2)) : registrationFee;

    // Calculate total fee
    const totalFee = reviewFee + registrationFeeAfterDiscount + subcategoryFee;

    // Update UI
    reviewFeeElement.textContent = `${reviewFee} OMR`;
    registrationFeeElement.textContent = `${registrationFeeAfterDiscount} OMR`;
    subcategoryFeeElement.textContent = `${subcategoryFee} OMR`;
    totalFeeElement.textContent = `${totalFee} OMR`;
  }

  // Event listeners
  companyGradeSelect.addEventListener('change', function() {
    adjustConsultancyOption();
    calculateFees();
  });
  categoryTypeSelect.addEventListener('change', calculateFees);
  numSubcategoriesInput.addEventListener('input', calculateFees);
  registrationDurationSelect.addEventListener('change', calculateFees);
  reyadaCardCheckbox.addEventListener('change', function() {
    if (reyadaCardCheckbox.checked) {
      registrationDurationSelect.value = 2;
      registrationDurationSelect.disabled = true;
    } else {
      registrationDurationSelect.disabled = false;
    }
    calculateFees();
  });

  // Initial calculation and adjustment
  adjustConsultancyOption();
  calculateFees();
});
