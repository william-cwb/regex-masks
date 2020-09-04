# regex-masks

## Javascript

```
export const unMaskDocument = (docuemnt) => {
    return docuemnt.replace(/[^0-9]+/g, "");
}

export const unMaskCep = (cep) => {
    return cep.replace("-", "");
}

export const maskCpf = (cpf) => {
    return cpf.replace(/(\d{3})(\d{3})(\d{3})(\d{2})/g, "\$1.\$2.\$3-\$4");
}

export const maskCnpj = (cnpj) => {
    return cnpj.replace(/(\d{2})(\d{3})(\d{3})(\d{4})(\d{2})/g, "\$1.\$2.\$3/\$4-\$5");
}

export const maskCep = (cep) => {
    return cep.replace(/(\d{5})(\d{3})/g, "\$1-\$2");
}

export const maskPhone = (phone) => {
    phone = phone.replace(/\D/g, "");
    phone = phone.replace(/^(\d{2})(\d)/g, "($1) $2");
    phone = phone.replace(/(\d)(\d{4})$/, "$1-$2");
    return phone
}
```
