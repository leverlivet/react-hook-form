## API Report File for "react-hook-form"

> Do not edit this file. It is a report generated by [API Extractor](https://api-extractor.com/).

```ts

/// <reference types="react" />

import { JSXElementConstructor } from 'react';
import { default as React_2 } from 'react';
import { ReactElement } from 'react';

// @public (undocumented)
export const appendErrors: (name: InternalFieldName, validateAllFieldCriteria: boolean, errors: InternalFieldErrors, type: string, message: ValidateResult) => {};

// Warning: (ae-forgotten-export) The symbol "IsTuple" needs to be exported by the entry point index.d.ts
// Warning: (ae-forgotten-export) The symbol "TupleKey" needs to be exported by the entry point index.d.ts
// Warning: (ae-forgotten-export) The symbol "ArrayPathImpl" needs to be exported by the entry point index.d.ts
// Warning: (ae-forgotten-export) The symbol "ArrayKey" needs to be exported by the entry point index.d.ts
//
// @public (undocumented)
export type ArrayPath<T> = T extends ReadonlyArray<infer V> ? IsTuple<T> extends true ? {
    [K in TupleKey<T>]-?: ArrayPathImpl<K & string, T[K]>;
}[TupleKey<T>] : ArrayPathImpl<ArrayKey, V> : {
    [K in keyof T]-?: ArrayPathImpl<K & string, T[K]>;
}[keyof T];

// @public (undocumented)
export type BatchFieldArrayUpdate = <T extends Function, TFieldValues, TFieldArrayName extends FieldArrayPath<TFieldValues> = FieldArrayPath<TFieldValues>, TKeyName extends string = 'id'>(name: InternalFieldName, method: T, args: {
    argA?: unknown;
    argB?: unknown;
}, updatedFieldArrayValues?: Partial<FieldArrayWithId<TFieldValues, TFieldArrayName, TKeyName>>[], shouldSetValue?: boolean, shouldSetFields?: boolean, shouldSetError?: boolean) => void;

// @public (undocumented)
export type ChangeHandler = (event: {
    target: any;
    type?: any;
}) => Promise<void | boolean>;

// @public (undocumented)
export type Control<TFieldValues extends FieldValues = FieldValues, TContext extends object = object> = {
    _subjects: Subjects<TFieldValues>;
    _removeUnmounted: Noop;
    _names: Names;
    _stateFlags: {
        mount: boolean;
        action: boolean;
        watch: boolean;
    };
    _options: UseFormProps<TFieldValues, TContext>;
    _getDirty: GetIsDirty;
    _formState: FormState<TFieldValues>;
    _updateValid: Noop;
    _fields: FieldRefs;
    _formValues: FieldValues;
    _proxyFormState: ReadFormState;
    _defaultValues: Partial<DefaultValues<TFieldValues>>;
    _getWatch: WatchInternal<TFieldValues>;
    _updateFieldArray: BatchFieldArrayUpdate;
    _getFieldArray: <TFieldArrayValues>(name: InternalFieldName) => Partial<TFieldArrayValues>[];
    _executeSchema: (names: InternalFieldName[]) => Promise<{
        errors: FieldErrors;
    }>;
    register: UseFormRegister<TFieldValues>;
    unregister: UseFormUnregister<TFieldValues>;
};

// @public (undocumented)
export const Controller: <TFieldValues extends FieldValues = FieldValues, TName extends Path<TFieldValues> = Path<TFieldValues>>(props: ControllerProps<TFieldValues, TName>) => ReactElement<any, string | JSXElementConstructor<any>>;

// @public (undocumented)
export type ControllerFieldState = {
    invalid: boolean;
    isTouched: boolean;
    isDirty: boolean;
    error?: FieldError;
};

// @public (undocumented)
export type ControllerProps<TFieldValues extends FieldValues = FieldValues, TName extends FieldPath<TFieldValues> = FieldPath<TFieldValues>> = {
    render: ({ field, fieldState, formState, }: {
        field: ControllerRenderProps<TFieldValues, TName>;
        fieldState: ControllerFieldState;
        formState: UseFormStateReturn<TFieldValues>;
    }) => React_2.ReactElement;
} & UseControllerProps<TFieldValues, TName>;

// @public (undocumented)
export type ControllerRenderProps<TFieldValues extends FieldValues = FieldValues, TName extends FieldPath<TFieldValues> = FieldPath<TFieldValues>> = {
    onChange: (...event: any[]) => void;
    onBlur: Noop;
    value: UnpackNestedValue<FieldPathValue<TFieldValues, TName>>;
    name: TName;
    ref: RefCallBack;
};

// @public (undocumented)
export type CriteriaMode = 'firstError' | 'all';

// @public (undocumented)
export type CustomElement<TFieldValues extends FieldValues> = {
    name: FieldName<TFieldValues>;
    type?: string;
    value?: any;
    disabled?: boolean;
    checked?: boolean;
    options?: HTMLOptionsCollection;
    files?: FileList | null;
    focus?: Noop;
};

// Warning: (ae-forgotten-export) The symbol "FileList" needs to be exported by the entry point index.d.ts
// Warning: (ae-forgotten-export) The symbol "File" needs to be exported by the entry point index.d.ts
//
// @public (undocumented)
export type DeepMap<T, TValue> = IsAny<T> extends true ? any : T extends Date | FileList_2 | File_2 | NestedValue ? TValue : T extends object ? {
    [K in keyof T]: DeepMap<NonUndefined<T[K]>, TValue>;
} : TValue;

// @public (undocumented)
export type DeepPartial<T> = T extends Date | FileList_2 | File_2 | NestedValue ? T : {
    [K in keyof T]?: DeepPartial<T[K]>;
};

// @public (undocumented)
export type DeepPartialSkipArrayKey<T> = T extends Date | FileList_2 | File_2 | NestedValue ? T : T extends ReadonlyArray<any> ? {
    [K in keyof T]: DeepPartialSkipArrayKey<T[K]>;
} : {
    [K in keyof T]?: DeepPartialSkipArrayKey<T[K]>;
};

// @public (undocumented)
export type DefaultValues<TFieldValues> = UnpackNestedValue<DeepPartial<TFieldValues>>;

// @public (undocumented)
export type DelayCallback = (name: InternalFieldName, error: FieldError) => void;

// @public (undocumented)
export type EmptyObject = {
    [K in string | number]: never;
};

// @public (undocumented)
export type ErrorOption = {
    message?: Message;
    type?: LiteralUnion<keyof RegisterOptions, string>;
    types?: MultipleFieldErrors;
};

// @public (undocumented)
export type EventType = 'focus' | 'blur' | 'change' | 'changeText' | 'valueChange' | 'contentSizeChange' | 'endEditing' | 'keyPress' | 'submitEditing' | 'layout' | 'selectionChange' | 'longPress' | 'press' | 'pressIn' | 'pressOut' | 'momentumScrollBegin' | 'momentumScrollEnd' | 'scroll' | 'scrollBeginDrag' | 'scrollEndDrag' | 'load' | 'error' | 'progress' | 'custom';

// @public (undocumented)
export type Field = {
    _f: {
        ref: Ref;
        name: InternalFieldName;
        refs?: HTMLInputElement[];
        mount?: boolean;
    } & RegisterOptions;
};

// @public (undocumented)
export type FieldArray<TFieldValues extends FieldValues = FieldValues, TFieldArrayName extends FieldArrayPath<TFieldValues> = FieldArrayPath<TFieldValues>> = FieldArrayPathValue<TFieldValues, TFieldArrayName> extends ReadonlyArray<infer U> | null | undefined ? U : never;

// @public (undocumented)
export type FieldArrayMethodProps = {
    shouldFocus?: boolean;
    focusIndex?: number;
    focusName?: string;
};

// @public (undocumented)
export type FieldArrayName = string;

// @public (undocumented)
export type FieldArrayPath<TFieldValues extends FieldValues> = ArrayPath<TFieldValues>;

// @public (undocumented)
export type FieldArrayPathValue<TFieldValues extends FieldValues, TFieldArrayPath extends FieldArrayPath<TFieldValues>> = PathValue<TFieldValues, TFieldArrayPath>;

// @public (undocumented)
export type FieldArrayWithId<TFieldValues extends FieldValues = FieldValues, TFieldArrayName extends FieldArrayPath<TFieldValues> = FieldArrayPath<TFieldValues>, TKeyName extends string = 'id'> = FieldArray<TFieldValues, TFieldArrayName> & Record<TKeyName, string>;

// @public (undocumented)
export type FieldElement<TFieldValues extends FieldValues = FieldValues> = HTMLInputElement | HTMLSelectElement | HTMLTextAreaElement | CustomElement<TFieldValues>;

// @public (undocumented)
export type FieldError = {
    type: LiteralUnion<keyof RegisterOptions, string>;
    ref?: Ref;
    types?: MultipleFieldErrors;
    message?: Message;
};

// @public (undocumented)
export type FieldErrors<TFieldValues extends FieldValues = FieldValues> = DeepMap<DeepPartial<TFieldValues>, FieldError>;

// @public (undocumented)
export type FieldName<TFieldValues extends FieldValues> = IsFlatObject<TFieldValues> extends true ? Extract<keyof TFieldValues, string> : string;

// @public (undocumented)
export type FieldNamesMarkedBoolean<TFieldValues extends FieldValues> = DeepMap<DeepPartial<TFieldValues>, boolean>;

// @public (undocumented)
export type FieldPath<TFieldValues extends FieldValues> = Path<TFieldValues>;

// @public (undocumented)
export type FieldPathValue<TFieldValues extends FieldValues, TFieldPath extends FieldPath<TFieldValues>> = PathValue<TFieldValues, TFieldPath>;

// @public (undocumented)
export type FieldPathValues<TFieldValues extends FieldValues, TPath extends FieldPath<TFieldValues>[] | readonly FieldPath<TFieldValues>[]> = {} & {
    [K in keyof TPath]: FieldPathValue<TFieldValues, TPath[K] & FieldPath<TFieldValues>>;
};

// @public (undocumented)
export type FieldRefs = Partial<Record<InternalFieldName, Field>>;

// @public (undocumented)
export type FieldValue<TFieldValues extends FieldValues> = TFieldValues[InternalFieldName];

// @public (undocumented)
export type FieldValues = Record<string, any>;

// @public (undocumented)
export const FormProvider: <TFieldValues extends FieldValues, TContext extends object = object>(props: FormProviderProps<TFieldValues, TContext>) => JSX.Element;

// @public (undocumented)
export type FormProviderProps<TFieldValues extends FieldValues = FieldValues, TContext extends object = object> = {
    children: React_2.ReactNode;
} & UseFormReturn<TFieldValues, TContext>;

// @public (undocumented)
export type FormState<TFieldValues> = {
    isDirty: boolean;
    dirtyFields: FieldNamesMarkedBoolean<TFieldValues>;
    isSubmitted: boolean;
    isSubmitSuccessful: boolean;
    submitCount: number;
    touchedFields: FieldNamesMarkedBoolean<TFieldValues>;
    isSubmitting: boolean;
    isValidating: boolean;
    isValid: boolean;
    errors: FieldErrors<TFieldValues>;
};

// @public (undocumented)
export type FormStateProxy<TFieldValues extends FieldValues = FieldValues> = {
    isDirty: boolean;
    isValidating: boolean;
    dirtyFields: FieldNamesMarkedBoolean<TFieldValues>;
    touchedFields: FieldNamesMarkedBoolean<TFieldValues>;
    errors: boolean;
    isValid: boolean;
};

// Warning: (ae-forgotten-export) The symbol "Subject" needs to be exported by the entry point index.d.ts
//
// @public (undocumented)
export type FormStateSubjectRef<TFieldValues> = Subject<Partial<FormState<TFieldValues>> & {
    name?: InternalFieldName;
}>;

// @public (undocumented)
export const get: <T>(obj: T, path: string, defaultValue?: unknown) => any;

// @public (undocumented)
export type GetIsDirty = <TName extends InternalFieldName, TData>(name?: TName, data?: TData) => boolean;

// @public (undocumented)
export type InternalFieldErrors = Partial<Record<InternalFieldName, FieldError>>;

// @public (undocumented)
export type InternalFieldName = string;

// @public (undocumented)
export type InternalNameSet = Set<InternalFieldName>;

// @public (undocumented)
export type IsAny<T> = boolean extends (T extends never ? true : false) ? true : false;

// @public (undocumented)
export type IsFlatObject<T extends object> = Extract<Exclude<T[keyof T], NestedValue | Date | FileList_2>, any[] | object> extends never ? true : false;

// @public (undocumented)
export type KeepStateOptions = Partial<{
    keepErrors: boolean;
    keepDirty: boolean;
    keepValues: boolean;
    keepDefaultValues: boolean;
    keepIsSubmitted: boolean;
    keepTouched: boolean;
    keepIsValid: boolean;
    keepSubmitCount: boolean;
}>;

// @public (undocumented)
export type LiteralUnion<T extends U, U extends Primitive> = T | (U & {
    _?: never;
});

// @public (undocumented)
export type Message = string;

// @public (undocumented)
export type Mode = keyof ValidationMode;

// @public (undocumented)
export type MultipleFieldErrors = {
    [K in keyof RegisterOptions]?: ValidateResult;
} & {
    [key: string]: ValidateResult;
};

// @public (undocumented)
export type Names = {
    mount: InternalNameSet;
    unMount: InternalNameSet;
    array: InternalNameSet;
    watch: InternalNameSet;
    focus: InternalFieldName;
    watchAll: boolean;
};

// @public (undocumented)
export type NativeFieldValue = string | number | boolean | null | undefined;

// @public (undocumented)
export type NestedValue<TValue extends object = object> = {
    [$NestedValue]: never;
} & TValue;

// @public (undocumented)
export type NonUndefined<T> = T extends undefined ? never : T;

// @public (undocumented)
export type Noop = () => void;

// Warning: (ae-forgotten-export) The symbol "PathImpl" needs to be exported by the entry point index.d.ts
//
// @public (undocumented)
export type Path<T> = T extends ReadonlyArray<infer V> ? IsTuple<T> extends true ? {
    [K in TupleKey<T>]-?: PathImpl<K & string, T[K]>;
}[TupleKey<T>] : PathImpl<ArrayKey, V> : {
    [K in keyof T]-?: PathImpl<K & string, T[K]>;
}[keyof T];

// @public (undocumented)
export type PathValue<T, P extends Path<T> | ArrayPath<T>> = T extends any ? P extends `${infer K}.${infer R}` ? K extends keyof T ? R extends Path<T[K]> ? PathValue<T[K], R> : never : K extends `${ArrayKey}` ? T extends ReadonlyArray<infer V> ? PathValue<V, R & Path<V>> : never : never : P extends keyof T ? T[P] : P extends `${ArrayKey}` ? T extends ReadonlyArray<infer V> ? V : never : never : never;

// @public (undocumented)
export type Primitive = null | undefined | string | number | boolean | symbol | bigint;

// @public (undocumented)
export type ReadFormState = {
    [K in keyof FormStateProxy]: boolean | 'all';
};

// @public (undocumented)
export type Ref = FieldElement;

// @public (undocumented)
export type RefCallBack = (instance: any) => void;

// @public (undocumented)
export type RegisterOptions<TFieldValues extends FieldValues = FieldValues, TFieldName extends FieldPath<TFieldValues> = FieldPath<TFieldValues>> = Partial<{
    required: Message | ValidationRule<boolean>;
    min: ValidationRule<number | string>;
    max: ValidationRule<number | string>;
    maxLength: ValidationRule<number>;
    minLength: ValidationRule<number>;
    pattern: ValidationRule<RegExp>;
    validate: Validate<FieldPathValue<TFieldValues, TFieldName>> | Record<string, Validate<FieldPathValue<TFieldValues, TFieldName>>>;
    valueAsNumber: boolean;
    valueAsDate: boolean;
    value: FieldPathValue<TFieldValues, TFieldName>;
    setValueAs: (value: any) => any;
    shouldUnregister?: boolean;
    onChange?: (event: any) => void;
    onBlur?: (event: any) => void;
    disabled: boolean;
    deps: InternalFieldName[];
}>;

// @public (undocumented)
export type Resolver<TFieldValues extends FieldValues = FieldValues, TContext extends object = object> = (values: UnpackNestedValue<TFieldValues>, context: TContext | undefined, options: ResolverOptions<TFieldValues>) => Promise<ResolverResult<TFieldValues>> | ResolverResult<TFieldValues>;

// @public (undocumented)
export type ResolverError<TFieldValues extends FieldValues = FieldValues> = {
    values: {};
    errors: FieldErrors<TFieldValues>;
};

// @public (undocumented)
export interface ResolverOptions<TFieldValues> {
    // (undocumented)
    criteriaMode?: CriteriaMode;
    // (undocumented)
    fields: Record<InternalFieldName, Field['_f']>;
    // (undocumented)
    names?: FieldName<TFieldValues>[];
    // (undocumented)
    shouldUseNativeValidation: boolean | undefined;
}

// @public (undocumented)
export type ResolverResult<TFieldValues extends FieldValues = FieldValues> = ResolverSuccess<TFieldValues> | ResolverError<TFieldValues>;

// @public (undocumented)
export type ResolverSuccess<TFieldValues extends FieldValues = FieldValues> = {
    values: UnpackNestedValue<TFieldValues>;
    errors: {};
};

// @public (undocumented)
export function set(object: FieldValues, path: string, value?: unknown): FieldValues;

// @public (undocumented)
export type SetFieldValue<TFieldValues> = FieldValue<TFieldValues>;

// @public (undocumented)
export type SetValueConfig = Partial<{
    shouldValidate: boolean;
    shouldDirty: boolean;
    shouldTouch: boolean;
}>;

// @public (undocumented)
export type Subjects<TFieldValues extends FieldValues = FieldValues> = {
    watch: Subject<{
        name?: InternalFieldName;
        type?: EventType;
        values?: FieldValues;
    }>;
    array: Subject<{
        name?: InternalFieldName;
        values?: FieldValues;
    }>;
    state: FormStateSubjectRef<TFieldValues>;
};

// @public (undocumented)
export type SubmitErrorHandler<TFieldValues extends FieldValues> = (errors: FieldErrors<TFieldValues>, event?: React_2.BaseSyntheticEvent) => any | Promise<any>;

// @public (undocumented)
export type SubmitHandler<TFieldValues extends FieldValues> = (data: UnpackNestedValue<TFieldValues>, event?: React_2.BaseSyntheticEvent) => any | Promise<any>;

// @public (undocumented)
export type TriggerConfig = Partial<{
    shouldFocus: boolean;
}>;

// @public (undocumented)
export type UnpackNestedValue<T> = T extends NestedValue<infer U> ? U : T extends Date | FileList | File ? T : T extends object ? {
    [K in keyof T]: UnpackNestedValue<T[K]>;
} : T;

// @public (undocumented)
export function useController<TFieldValues extends FieldValues = FieldValues, TName extends FieldPath<TFieldValues> = FieldPath<TFieldValues>>(props: UseControllerProps<TFieldValues, TName>): UseControllerReturn<TFieldValues, TName>;

// @public (undocumented)
export type UseControllerProps<TFieldValues extends FieldValues = FieldValues, TName extends FieldPath<TFieldValues> = FieldPath<TFieldValues>> = {
    name: TName;
    rules?: Omit<RegisterOptions<TFieldValues, TName>, 'valueAsNumber' | 'valueAsDate' | 'setValueAs' | 'disabled'>;
    shouldUnregister?: boolean;
    defaultValue?: UnpackNestedValue<FieldPathValue<TFieldValues, TName>>;
    control?: Control<TFieldValues>;
};

// @public (undocumented)
export type UseControllerReturn<TFieldValues extends FieldValues = FieldValues, TName extends FieldPath<TFieldValues> = FieldPath<TFieldValues>> = {
    field: ControllerRenderProps<TFieldValues, TName>;
    formState: UseFormStateReturn<TFieldValues>;
    fieldState: ControllerFieldState;
};

// @public (undocumented)
export const useFieldArray: <TFieldValues extends FieldValues = FieldValues, TFieldArrayName extends ArrayPath<TFieldValues> = ArrayPath<TFieldValues>, TKeyName extends string = "id">(props: UseFieldArrayProps<TFieldValues, TFieldArrayName, TKeyName>) => UseFieldArrayReturn<TFieldValues, TFieldArrayName, TKeyName>;

// @public (undocumented)
export type UseFieldArrayProps<TFieldValues extends FieldValues = FieldValues, TFieldArrayName extends FieldArrayPath<TFieldValues> = FieldArrayPath<TFieldValues>, TKeyName extends string = 'id'> = {
    name: TFieldArrayName;
    keyName?: TKeyName;
    control?: Control<TFieldValues>;
    shouldUnregister?: boolean;
};

// @public (undocumented)
export type UseFieldArrayReturn<TFieldValues extends FieldValues = FieldValues, TFieldArrayName extends FieldArrayPath<TFieldValues> = FieldArrayPath<TFieldValues>, TKeyName extends string = 'id'> = {
    swap: (indexA: number, indexB: number) => void;
    move: (indexA: number, indexB: number) => void;
    prepend: (value: Partial<FieldArray<TFieldValues, TFieldArrayName>> | Partial<FieldArray<TFieldValues, TFieldArrayName>>[], options?: FieldArrayMethodProps) => void;
    append: (value: Partial<FieldArray<TFieldValues, TFieldArrayName>> | Partial<FieldArray<TFieldValues, TFieldArrayName>>[], options?: FieldArrayMethodProps) => void;
    remove: (index?: number | number[]) => void;
    insert: (index: number, value: Partial<FieldArray<TFieldValues, TFieldArrayName>> | Partial<FieldArray<TFieldValues, TFieldArrayName>>[], options?: FieldArrayMethodProps) => void;
    update: (index: number, value: Partial<FieldArray<TFieldValues, TFieldArrayName>>) => void;
    replace: (value: Partial<FieldArray<TFieldValues, TFieldArrayName>> | Partial<FieldArray<TFieldValues, TFieldArrayName>>[]) => void;
    fields: FieldArrayWithId<TFieldValues, TFieldArrayName, TKeyName>[];
};

// @public (undocumented)
export function useForm<TFieldValues extends FieldValues = FieldValues, TContext extends object = object>(props?: UseFormProps<TFieldValues, TContext>): UseFormReturn<TFieldValues, TContext>;

// @public (undocumented)
export type UseFormClearErrors<TFieldValues extends FieldValues> = (name?: FieldPath<TFieldValues> | FieldPath<TFieldValues>[] | readonly FieldPath<TFieldValues>[]) => void;

// @public (undocumented)
export const useFormContext: <TFieldValues extends FieldValues>() => UseFormReturn<TFieldValues, object>;

// @public (undocumented)
export type UseFormGetValues<TFieldValues extends FieldValues> = {
    (): UnpackNestedValue<TFieldValues>;
    <TFieldName extends FieldPath<TFieldValues>>(name: TFieldName): FieldPathValue<TFieldValues, TFieldName>;
    <TFieldNames extends FieldPath<TFieldValues>[]>(names: readonly [...TFieldNames]): [...FieldPathValues<TFieldValues, TFieldNames>];
};

// @public (undocumented)
export type UseFormHandleSubmit<TFieldValues extends FieldValues> = <TSubmitFieldValues extends FieldValues = TFieldValues>(onValid: SubmitHandler<TSubmitFieldValues>, onInvalid?: SubmitErrorHandler<TFieldValues>) => (e?: React_2.BaseSyntheticEvent) => Promise<void>;

// @public (undocumented)
export type UseFormProps<TFieldValues extends FieldValues = FieldValues, TContext extends object = object> = Partial<{
    mode: Mode;
    reValidateMode: Exclude<Mode, 'onTouched' | 'all'>;
    defaultValues: DefaultValues<TFieldValues>;
    resolver: Resolver<TFieldValues, TContext>;
    context: TContext;
    shouldFocusError: boolean;
    shouldUnregister: boolean;
    shouldUseNativeValidation: boolean;
    criteriaMode: CriteriaMode;
    delayError: number;
}>;

// @public (undocumented)
export type UseFormRegister<TFieldValues extends FieldValues> = <TFieldName extends FieldPath<TFieldValues> = FieldPath<TFieldValues>>(name: TFieldName, options?: RegisterOptions<TFieldValues, TFieldName>) => UseFormRegisterReturn;

// @public (undocumented)
export type UseFormRegisterReturn = {
    onChange: ChangeHandler;
    onBlur: ChangeHandler;
    ref: RefCallBack;
    name: InternalFieldName;
    min?: string | number;
    max?: string | number;
    maxLength?: number;
    minLength?: number;
    pattern?: string;
    required?: boolean;
    disabled?: boolean;
};

// @public (undocumented)
export type UseFormReset<TFieldValues extends FieldValues> = (values?: DefaultValues<TFieldValues> | UnpackNestedValue<TFieldValues>, keepStateOptions?: KeepStateOptions) => void;

// @public (undocumented)
export type UseFormResetField<TFieldValues extends FieldValues> = <TFieldName extends FieldPath<TFieldValues> = FieldPath<TFieldValues>>(name: TFieldName, options?: Partial<{
    keepDirty: boolean;
    keepTouched: boolean;
    keepError: boolean;
    defaultValue: any;
}>) => void;

// @public (undocumented)
export type UseFormReturn<TFieldValues extends FieldValues = FieldValues, TContext extends object = object> = {
    watch: UseFormWatch<TFieldValues>;
    getValues: UseFormGetValues<TFieldValues>;
    setError: UseFormSetError<TFieldValues>;
    clearErrors: UseFormClearErrors<TFieldValues>;
    setValue: UseFormSetValue<TFieldValues>;
    trigger: UseFormTrigger<TFieldValues>;
    formState: FormState<TFieldValues>;
    resetField: UseFormResetField<TFieldValues>;
    reset: UseFormReset<TFieldValues>;
    handleSubmit: UseFormHandleSubmit<TFieldValues>;
    unregister: UseFormUnregister<TFieldValues>;
    control: Control<TFieldValues, TContext>;
    register: UseFormRegister<TFieldValues>;
    setFocus: UseFormSetFocus<TFieldValues>;
};

// @public (undocumented)
export type UseFormSetError<TFieldValues extends FieldValues> = (name: FieldPath<TFieldValues>, error: ErrorOption, options?: {
    shouldFocus: boolean;
}) => void;

// @public (undocumented)
export type UseFormSetFocus<TFieldValues extends FieldValues> = <TFieldName extends FieldPath<TFieldValues> = FieldPath<TFieldValues>>(name: TFieldName) => void;

// @public (undocumented)
export type UseFormSetValue<TFieldValues extends FieldValues> = <TFieldName extends FieldPath<TFieldValues> = FieldPath<TFieldValues>>(name: TFieldName, value: UnpackNestedValue<FieldPathValue<TFieldValues, TFieldName>>, options?: SetValueConfig) => void;

// @public (undocumented)
export function useFormState<TFieldValues extends FieldValues = FieldValues>(props?: UseFormStateProps<TFieldValues>): UseFormStateReturn<TFieldValues>;

// @public (undocumented)
export type UseFormStateProps<TFieldValues> = Partial<{
    control?: Control<TFieldValues>;
    disabled?: boolean;
    name?: FieldPath<TFieldValues> | FieldPath<TFieldValues>[] | readonly FieldPath<TFieldValues>[];
    exact?: boolean;
}>;

// @public (undocumented)
export type UseFormStateReturn<TFieldValues> = FormState<TFieldValues>;

// @public (undocumented)
export type UseFormTrigger<TFieldValues extends FieldValues> = (name?: FieldPath<TFieldValues> | FieldPath<TFieldValues>[] | readonly FieldPath<TFieldValues>[], options?: TriggerConfig) => Promise<boolean>;

// @public (undocumented)
export type UseFormUnregister<TFieldValues extends FieldValues> = (name?: FieldPath<TFieldValues> | FieldPath<TFieldValues>[] | readonly FieldPath<TFieldValues>[], options?: Omit<KeepStateOptions, 'keepIsSubmitted' | 'keepSubmitCount' | 'keepValues' | 'keepDefaultValues' | 'keepErrors'> & {
    keepValue?: boolean;
    keepDefaultValue?: boolean;
    keepError?: boolean;
}) => void;

// @public (undocumented)
export type UseFormWatch<TFieldValues extends FieldValues> = {
    (): UnpackNestedValue<TFieldValues>;
    <TFieldName extends FieldPath<TFieldValues>>(name: TFieldName, defaultValue?: FieldPathValue<TFieldValues, TFieldName>): FieldPathValue<TFieldValues, TFieldName>;
    <TFieldNames extends readonly FieldPath<TFieldValues>[]>(names: readonly [...TFieldNames], defaultValue?: UnpackNestedValue<DeepPartial<TFieldValues>>): FieldPathValues<TFieldValues, TFieldNames>;
    (callback: WatchObserver<TFieldValues>, defaultValues?: UnpackNestedValue<DeepPartial<TFieldValues>>): Subscription;
};

// @public (undocumented)
export function useWatch<TFieldValues extends FieldValues = FieldValues>(props: {
    defaultValue?: UnpackNestedValue<DeepPartialSkipArrayKey<TFieldValues>>;
    control?: Control<TFieldValues>;
    disabled?: boolean;
    exact?: boolean;
}): UnpackNestedValue<DeepPartialSkipArrayKey<TFieldValues>>;

// @public (undocumented)
export function useWatch<TFieldValues extends FieldValues = FieldValues, TFieldName extends FieldPath<TFieldValues> = FieldPath<TFieldValues>>(props: {
    name: TFieldName;
    defaultValue?: FieldPathValue<TFieldValues, TFieldName>;
    control?: Control<TFieldValues>;
    disabled?: boolean;
    exact?: boolean;
}): FieldPathValue<TFieldValues, TFieldName>;

// @public (undocumented)
export function useWatch<TFieldValues extends FieldValues = FieldValues, TFieldNames extends readonly FieldPath<TFieldValues>[] = readonly FieldPath<TFieldValues>[]>(props: {
    name: readonly [...TFieldNames];
    defaultValue?: UnpackNestedValue<DeepPartialSkipArrayKey<TFieldValues>>;
    control?: Control<TFieldValues>;
    disabled?: boolean;
    exact?: boolean;
}): FieldPathValues<TFieldValues, TFieldNames>;

// @public (undocumented)
export function useWatch<TFieldValues extends FieldValues = FieldValues, TFieldNames extends FieldPath<TFieldValues>[] = FieldPath<TFieldValues>[]>(): FieldPathValues<TFieldValues, TFieldNames>;

// @public (undocumented)
export type UseWatchProps<TFieldValues extends FieldValues = FieldValues> = {
    defaultValue?: unknown;
    disabled?: boolean;
    name?: FieldPath<TFieldValues> | FieldPath<TFieldValues>[] | readonly FieldPath<TFieldValues>[];
    control?: Control<TFieldValues>;
    exact?: boolean;
};

// @public (undocumented)
export type Validate<TFieldValue> = (value: TFieldValue) => ValidateResult | Promise<ValidateResult>;

// @public (undocumented)
export type ValidateResult = Message | Message[] | boolean | undefined;

// @public (undocumented)
export type ValidationMode = {
    onBlur: 'onBlur';
    onChange: 'onChange';
    onSubmit: 'onSubmit';
    onTouched: 'onTouched';
    all: 'all';
};

// @public (undocumented)
export type ValidationRule<TValidationValue extends ValidationValue = ValidationValue> = TValidationValue | ValidationValueMessage<TValidationValue>;

// @public (undocumented)
export type ValidationValue = boolean | number | string | RegExp;

// @public (undocumented)
export type ValidationValueMessage<TValidationValue extends ValidationValue = ValidationValue> = {
    value: TValidationValue;
    message: Message;
};

// @public (undocumented)
export type WatchInternal<TFieldValues> = (fieldNames?: InternalFieldName | InternalFieldName[], defaultValue?: UnpackNestedValue<DeepPartial<TFieldValues>>, isMounted?: boolean, isGlobal?: boolean) => FieldPathValue<FieldValues, InternalFieldName> | FieldPathValues<FieldValues, InternalFieldName[]>;

// @public (undocumented)
export type WatchObserver<TFieldValues> = (value: UnpackNestedValue<DeepPartial<TFieldValues>>, info: {
    name?: FieldPath<TFieldValues>;
    type?: EventType;
    value?: unknown;
}) => void;

// Warnings were encountered during analysis:
//
// src/types/form.ts:195:3 - (ae-forgotten-export) The symbol "Subscription" needs to be exported by the entry point index.d.ts

// (No @packageDocumentation comment for this package)

```
