# Pai para filho

```tsx
<Parent>
  <Children />
</Parent>
```

# Propriedade

```tsx
<Parent title="">
  <Children />
</Parent>
```

# Hooks (useState, useContext, useReducer)

```tsx
function Component() {
  const [state, setState] = useState()

}

```

# Fluxo de renderização

1. Gerar uma nova versão do componente que precisa ser renderizado;
2. Comparar essa nova versão com a versão anterior já salva na página;
3. Se houverem alterações, o React "renderiza" essa nova versão em tela;

---

## Memo

### Quando deve ser utilizado:

1. Pure Functional Components // dado os mesmos parâmetros sempre retornam o mesmo resultado.
2. Renders too often // componentes que renderizam muitas vezes.
3. Re-renders with same props. // componentes que renderizam com as mesmas props
4. Medium to big size. // Em componentes pequenos o memo não traz grandes ganhos para aplicação

## UseMemo

### Quando deve ser utilizado:

1. Cálculos pesados
2. Igualdade referencial // quando a gente repassa aquela informação a um componente filho







