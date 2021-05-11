# Fluxo de renderização no ReactJS

1. Gerar uma nova versão do componente que precisa ser renderizado;
2. Comparar essa nova versão com a versão anterior já salva na página;
3. Se houverem alterações, o React "renderiza" essa nova versão em tela;

# Situações que os componentes são renderizados:

## Pai para filho 
#### Quando o componente pai é renderizado

```tsx
<Parent>
  <Children />
</Parent>
```

## Propriedade
#### Quando uma propriedade é alterada
```tsx
<Parent title="">
  <Children />
</Parent>
```

## Hooks (useState, useContext, useReducer)
#### Quando um hook é executado

```tsx
function Component() {
  const [state, setState] = useState()

}

```
---

# Estratégias de otimização:

---

## Memo

### Quando deve ser utilizado:

1. Pure Functional Components // dado os mesmos parâmetros sempre retornam o mesmo resultado.
2. Renders too often // componentes que renderizam muitas vezes.
3. Re-renders with same props. // componentes que renderizam com as mesmas props
4. Medium to big size. // Em componentes pequenos o memo não traz grandes ganhos para aplicação

## UseMemo

### Quando deve ser utilizado:

1. Cálculos pesados // o useMemo serve para armazenar um valor
2. Igualdade referencial // quando a gente repassa aquela informação a um componente filho

## UseCallback

### Quando deve ser utilizado:

Quando temos uma função que precisa ser repassada para os componentes filhos da nossa aplicação.








