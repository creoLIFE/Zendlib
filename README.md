Zendlib
=======

Zend Framework third-party libraries

1. ZF ORM library by Federico Cargnelutti (https://github.com/fedecarg/zf-packages/tree/master/Orm)

2. Main_Validator_SecurePassword
  Zend-like validator for secure password
  (source - http://stackoverflow.com/questions/11923891/is-there-any-custom-validator-for-password-zend-framework)

  Usage:
  <code>
  $passwordOpts = array('requireAlpha' => true,
                      'requireNumeric' => true,
                      'minPasswordLength' => 8);

  $pwValidator = new My_Validator_SecurePassword($passwordOpts);

  $password = new Zend_Form_Element_Password('password', array(
    'validators' => array($pwValidator),
    'description' => $pwValidator->getRequirementString(),
    'label' => 'Password:',
    'required' => true,
  ));
  </code>