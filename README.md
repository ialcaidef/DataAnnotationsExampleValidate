# DataAnnotationsExampleValidate
MOD06_DEMO_03

Ejemplo de uso de Data Annotations para realizar validaciones en el modelo

public class Person
    {
        public int PersonId { get; set; }

        [DataType(DataType.Text)]
        [Display(Name = "First Name:")]

        public string FirstName { get; set; }

        [DataType(DataType.Text)]
        [Display(Name = "Last Name:")]
        [Required(ErrorMessage = "Please enter your last name.")]
        public string LastName { get; set; }

        [Range(15, 50)]
        [Display(Name = "Age:")]
        public int Age { get; set; }

        [StringLength(10)]
        [Display(Name = "Description:")]
        public string Description { get; set; }
    }
    
    Tanto el enlace de modelos como la validación de modelos se producen antes de la ejecución de una acción de controlador o un Razor método de controlador de páginas. 
    En el caso de las aplicaciones web, la aplicación es responsable de inspeccionar ModelState.IsValid y reaccionar de manera apropiada. Normalmente, 
    las aplicaciones web vuelven a mostrar la página con un mensaje de error.
    
    Atributos integrados
    Estos son algunos de los atributos de validación integrados:
    
    [CreditCard]: Valida que la propiedad tiene un formato de tarjeta de crédito. Requiere métodos adicionales de validación de jQuery.  
    
    [Compare]: Valida que dos propiedades de un modelo coincidan.  
    
    [EmailAddress]: Valida que la propiedad tiene un formato de correo electrónico.  
    
    [Phone]: Valida que la propiedad tiene un formato de número de teléfono.  
    
    [Range]: Valida que el valor de la propiedad se encuentra dentro de un intervalo especificado.  
    
    [RegularExpression]: Valida que el valor de propiedad coincide con una expresión regular especificada.  
    
    [Required]: Valida que el campo no sea NULL. Vea el [Required] atributo para obtener más información sobre el comportamiento de este atributo.
    
    [StringLength]: Valida que un valor de propiedad de cadena no supera un límite de longitud especificado.  
    
    [Url]: Valida que la propiedad tiene un formato de dirección URL.  
    
    [Remote]: Valida la entrada en el cliente mediante una llamada a un método de acción en el servidor. 
    
